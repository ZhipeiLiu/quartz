# Kitsunebi draft











```

{
  "log": {
    "error": "",
    "loglevel": "info",
    "access": ""
  },
  "inbounds": [
    {
      "listen": "127.0.0.1",
      "protocol": "socks",
      "settings": {
        "udp": false,
        "auth": "noauth"
      },
      "port": "1080"
    },
    {
      "listen": "127.0.0.1",
      "protocol": "http",
      "settings": {
        "timeout": 360
      },
      "port": "1088"
    }
  ],
  "outbounds": [
    {
      "mux": {
        "enabled": false,
        "concurrency": 8
      },
      "protocol": "vmess",
      "streamSettings": {
        "wsSettings": {
          "path": "\/bilibili.com",
          "headers": {
            "host": ""
          }
        },
        "tlsSettings": {
          "allowInsecure": true
        },
        "security": "tls",
        "network": "ws"
      },
      "tag": "proxy",
      "settings": {
        "vnext": [
          {
            "address": "v.mattzo.com",
            "users": [
              {
                "id": "0efac691-48b5-44ec-d1f9-430f297aff4c",
                "alterId": 64,
                "level": 0,
                "security": "aes-128-gcm"
              }
            ],
            "port": 47001
          }
        ]
      }
    },
    {
      "tag": "direct",
      "protocol": "freedom",
      "settings": {
        "domainStrategy": "UseIP",
        "redirect": "",
        "userLevel": 0
      }
    },
    {
      "tag": "block",
      "protocol": "blackhole",
      "settings": {
        "response": {
          "type": "none"
        }
      }
    }
  ],
  "dns": {
    "clientIp": "115.239.211.92",
    "hosts": {
      "localhost": "127.0.0.1"
    },
    "servers": [
      "114.114.114.114",
      {
        "address": "8.8.8.8",
        "domains": [
          "google",
          "android",
          "fbcdn",
          "facebook",
          "domain:fb.com",
          "instagram",
          "whatsapp",
          "akamai",
          "domain:line-scdn.net",
          "domain:line.me",
          "domain:naver.jp"
        ],
        "port": 53
      }
    ]
  },
  "routing": {
    "domainStrategy": "IPOnDemand",
    "rules": [
      {
        "type": "field",
        "ip": [
          "geoip:private"
        ],
        "outboundTag": "direct"
      }
    ]
  },
  "transport": {}
}

```





## app template
`
{
  "outbounds": [
    {
      "protocol": "vmess",
      "settings": {
        "vnext": [
          {
            "address": "1.2.3.4",
            "port": 10086,
            "users": [
              {
                "id": "0e8575fb-a71f-455b-877f-b74e19d3f495"
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "tcp"
      },
      "tag": "proxy"
    },
    {
      "protocol": "freedom",
      "settings": {
        "domainStrategy": "UseIP"
      },
      "streamSettings": {},
      "tag": "direct"
    },
    {
      "protocol": "blackhole",
      "settings": {},
      "tag": "block"
    },
    {
      "protocol": "dns",
      "tag": "dns-out"
    }
  ],
  "dns": {
    "clientIp": "115.239.211.92",
    "hosts": {
      "localhost": "127.0.0.1"
    },
    "servers": [
      "114.114.114.114",
      {
        "address": "8.8.8.8",
        "domains": [
          "google",
          "android",
          "fbcdn",
          "facebook",
          "domain:fb.com",
          "instagram",
          "whatsapp",
          "akamai",
          "domain:line-scdn.net",
          "domain:line.me",
          "domain:naver.jp"
        ],
        "port": 53
      }
    ]
  },
  "log": {
    "error": "",
    "loglevel": "info"
    "access": ""
  },
  "policy": {
    "levels": {
      "0": {
        "bufferSize": 4096,
        "connIdle": 30,
        "downlinkOnly": 0,
        "handshake": 4,
        "uplinkOnly": 0
      }
    }
  },
  "routing": {
    "domainStrategy": "IPIfNonMatch",
    "rules": [
      {
        "inboundTag": [
          "tun2socks"
        ],
        "network": "udp",
        "port": 53,
        "outboundTag": "dns-out",
        "type": "field"
      },
      {
        "domain": [
          "domain:setup.icloud.com"
        ],
        "outboundTag": "proxy",
        "type": "field"
      },
      {
        "ip": [
          "8.8.8.8\/32",
          "8.8.4.4\/32",
          "1.1.1.1\/32",
          "1.0.0.1\/32",
          "9.9.9.9\/32",
          "149.112.112.112\/32",
          "208.67.222.222\/32",
          "208.67.220.220\/32"
        ],
        "outboundTag": "proxy",
        "type": "field"
      },
      {
        "ip": [
          "geoip:cn",
          "geoip:private"
        ],
        "outboundTag": "direct",
        "type": "field"
      },
      {
        "outboundTag": "direct",
        "port": "123",
        "type": "field"
      },
      {
        "domain": [
          "domain:pstatp.com",
          "domain:snssdk.com",
          "domain:toutiao.com",
          "domain:ixigua.com",
          "domain:apple.com",
          "domain:crashlytics.com",
          "domain:icloud.com",
          "cctv",
          "umeng",
          "domain:weico.cc",
          "domain:jd.com",
          "domain:360buy.com",
          "domain:360buyimg.com",
          "domain:douyu.tv",
          "domain:douyu.com",
          "domain:douyucdn.cn",
          "geosite:cn"
        ],
        "outboundTag": "direct",
        "type": "field"
      },
      {
        "ip": [
          "149.154.167.0\/24",
          "149.154.175.0\/24",
          "91.108.56.0\/24",
          "125.209.222.0\/24"
        ],
        "outboundTag": "proxy",
        "type": "field"
      },
      {
        "domain": [
          "twitter",
          "domain:twimg.com",
          "domain:t.co",
          "google",
          "domain:ggpht.com",
          "domain:gstatic.com",
          "domain:youtube.com",
          "domain:ytimg.com",
          "pixiv",
          "domain:pximg.net",
          "tumblr",
          "instagram",
          "domain:line-scdn.net",
          "domain:line.me",
          "domain:naver.jp",
          "domain:facebook.com",
          "domain:fbcdn.net",
          "pinterest",
          "github",
          "dropbox",
          "netflix",
          "domain:medium.com",
          "domain:fivecdm.com"
        ],
        "outboundTag": "proxy",
        "type": "field"
      }
    ],
    "strategy": "rules"
  }
}

`

## working in app
`
{
  "log": {
    "error": "",
    "loglevel": "info",
    "access": ""
  },
  "inbounds": [
    {
      "listen": "127.0.0.1",
      "protocol": "socks",
      "settings": {
        "udp": false,
        "auth": "noauth"
      },
      "port": "1080"
    },
    {
      "listen": "127.0.0.1",
      "protocol": "http",
      "settings": {
        "timeout": 360
      },
      "port": "1088"
    }
  ],
  "outbounds": [
    {
      "mux": {
        "enabled": false,
        "concurrency": 8
      },
      "protocol": "vmess",
      "streamSettings": {
        "wsSettings": {
          "path": "\/bilibili.com",
          "headers": {
            "host": ""
          }
        },
        "tlsSettings": {
          "allowInsecure": true
        },
        "security": "tls",
        "network": "ws"
      },
      "tag": "proxy",
      "settings": {
        "vnext": [
          {
            "address": "v.mattzo.com",
            "users": [
              {
                "id": "0efac691-48b5-44ec-d1f9-430f297aff4c",
                "alterId": 64
              }
            ],
            "port": 47001
          }
        ]
      }
    },
    {
      "tag": "direct",
      "protocol": "freedom",
      "settings": {
        "domainStrategy": "UseIP",
        "redirect": "",
        "userLevel": 0
      }
    },
    {
      "tag": "block",
      "protocol": "blackhole",
      "settings": {
        "response": {
          "type": "none"
        }
      }
    }
  ],
  "dns": {
    "clientIp": "115.239.211.92",
    "hosts": {
      "localhost": "127.0.0.1"
    },
    "servers": [
      "114.114.114.114",
      {
        "address": "8.8.8.8",
        "domains": [
          "google",
          "android",
          "fbcdn",
          "facebook",
          "domain:fb.com",
          "instagram",
          "whatsapp",
          "akamai",
          "domain:line-scdn.net",
          "domain:line.me",
          "domain:naver.jp"
        ],
        "port": 53
      }
    ]
  },
  "routing": {
    "domainStrategy": "IPOnDemand",
    "rules": [
      {
        "type": "field",
        "ip": [
          "geoip:private"
        ],
        "outboundTag": "direct"
      }
    ]
  },
  "transport": {}
}
`