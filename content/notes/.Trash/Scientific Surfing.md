Notes:
Sources: 
	[Shadowsocks检测与封锁及配置策略](https://project-gutenberg.github.io/Pincong/post/d01c8fbc6d354bc80048bc4c523f65c7/)
tags: #scientific-surfing #GFW #network

# [[Scientific Surfing]]

### Shadowsocks config
- 现在请务必使用AEAD加密的算法（chacha20-ietf-poly1305、xchacha20-ietf-poly1305、aes-128-gcm、aes-192-gcm、aes-256-gcm）
- 目前xchacha20-ietf-poly1305和aes-256-gcm是最佳的选择，由于各大平台的cpu现在对aes算法都有较好的优化，我个人推荐aes-256-gcm
- 在自行配置shadowsocks服务器的时候，很多攻略仍然写的是基于**Python**的shadowsocks-server，请不要再参考这些攻略！！！基于python的那个版本已经三年没有更新了，很多教程甚至还在用五年前的2.8.2版，请尽快转用C语言的shadowsocks-libev，githb地址：“[https://github.com/shadowsocks/shadowsocks-libev"](https://github.com/shadowsocks/shadowsocks-libev%22))



### PC端科学上网常见问题
https://hijk.pp.ua/pc-vpn-problem-faq/
https://medium.com/@bishopbriggsbus/v2ray-for-windows-users-with-v2rayn-e9d84f5f3a98