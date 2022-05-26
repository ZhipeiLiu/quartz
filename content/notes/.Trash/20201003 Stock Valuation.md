# [[20201003 Stock Valuation]]
Notes: 
		[[001 Corporate Fin Class Notes]] 
tags: #literature-note #finance #corpfin 

### Topics/Key Concepts/Key Questions
1. Variations of the dividend discount model (DDM)
2. Estimating parameters in the DDM
3. Valuation by comparables
4. Free cash flow valuation

### Learning Objectives
1. Solve for the value of a stock using all three versions of the dividend discount model (DDM)
2. Describe how to estimate the growth rate and required return for the DDM
3. Apply valuation by comparables in order to determine an appropriate price for a stock
4. Calculate enterprise value and stock price using free cash flow valuation

### Guiding Questions
1. How do the three versions of the dividend discount model differ from each other?
2. How can market multiples be used to estimate the value of a stock?
3. What factors should be considered when identifying comparable firms?
4. What is the conceptual difference between the dividend discount model and the free cash flow model?
5. What types of firms are best suited for each of the three valuation techniques (i.e., the dividend discount model, valuation by comparables, and free cash flow valuation)?

## Lectures
### Dividend Discount Model
- Measures the value per share of common stock based on the present value of all expected future dividends
- Accounts for both dividends and capital gains
- $P_0=\frac{D_1}{1+R}+\frac{D_2}{(1+R)^2}+\frac{D_3}{(1+R)^3}+... = \sum^{\infty}_{t=1}\frac{D_t}{(1+R)^t}$
- The general DDM can be simplified if dividends are expected to follow one of 3 different growth patterns
	![[Dividend growth patterns.png]]
	1. ==Zero growth==
		- Assumes an indefinite stream of constant dividends
			- $D_1 = D_2 = … = D$
		- Useful for valuing preferred stocks (constant dividend)
			- $P_0 = \frac{D_1}{1+R}+\frac{D_2}{(1+R)^2}+...=\frac{D}{R}$
	2. ==Constant growth==
		- Assumes an indefinite stream of dividends growing at a constant rate of g
		- Only valid when R > g
		- $P_0=\frac{D_1}{1+R}+\frac{D_1(1+g)}{(1+R)^2}+\frac{D_1(1+g)^2}{(1+R)^3}+\frac{D_1(1+g)^3}{(1+R)^4}+...=\frac{D_1}{R-g}$
	3. ==Differential growth==
		- Assumes two stages of dividend growth
			1. Periods 1 through T: a finite stream of dividends growing at a constant rate of g1 
			2. Periods T+1 through $\infty$: an indefinite stream of dividends growing at a constant rate of g2
		- $P_0 = \sum^T_{t=1} \frac{D(1+g_1)^t}{(1+R)^t}+\frac{P_T}{(1+R)^{T'}}$
			- where $P_T = \frac{D_{T+1}}{R-g_2}=\frac{D_T\times(1+g_2)}{R-g_2}$
		- Alternatively, the dividends in stage 1 may not grow at a constant rate

### Estimates of parameters in the DDM
- **Estimating Growth**
	- Growth requires a positive net investment (i.e., gross investment less depreciation) --> Some earnings must be retained
	- $Earnings_1 = Earnings_0 + Retained\ Earnings_0 \times Return\ on\ R/E$
	- $\frac{Earnings_1}{Earnings_0} = \frac{Earnings_0}{Earnings_0} + \frac{Retained\ Earnings_0}{Earnings_0} \times Return\ on\ R/E$
	- $1+g = 1+ Retention\ ratio \times Return\ on\ R/E$
	- ==$g = Retention\ ratio \times Return\ on\ R/E = Retention\ ratio \times ROE$==
	- if dividend payout ratio is held constant, then  $g_{earnings} = g_{dividends}$
- **Estimating the Required Return**
	- Can be derived from the constant growth DDM
	- $P_0 = \frac{D_1}{R-g}$
	- $R = \frac{D_1}{P_0}+g=Dividend\ yield+Capital\ gains\ yield$

### Valuation by comparables
- An alternative to discounted cash flow (DCF) valuation is valuation by comparables - AKA relative valuation 
	- Involves the use of multiples to value stocks based on how similar stocks are currently priced in the market
		- A multiple is a standardized estimate of value
		- $\frac{Measure\ of\ value}{Driver\ of\ value}$
- **Price-Earnings Ratio**
	- A measure of ==equity value== 
	- Can be computed using trailing or forward earnings
		- $PE\ ratio = \frac{P_0}{EPS}$
	- Often used to estimate a firm’s stock price based on the typical ratio among comparable firms
		- $P_0=Benchmark\ PE\ ratio \times EPS$
		- Comparable firms could be those in the same industry with similar characteristics
			1. Investment opportunities
			2. Risk
			3. Accounting practices
- **EV Multiple**
	- A measure of ==total firm value==
		- $EV\ multiple = \frac{Enterprise\ Value}{EBITDA}$
			- where	$Enterprise\ Value=Market\ value\ of\ equity+Market\ value\ of\ debt-Cash$
			- EBITDA = EBIT + D&A
			- Market value of debt can be approximated by its book value
	- Often used to estimate a firm’s enterprise value based on the typical ratio among comparable firms
		- $Enterprise\ Value=Benchmark\ EV\ multiple \times EBITDA$
		- $Enterprise\ value = Equity\ value+Debt-Cash$
		- $Equity\ value = Enterprise\ value-Debt+Cash$
- **Free Cash Flow (FCF) Valuation**
	- Used to value the ==entire equity of a firm==
		- $PV_0 = \frac{FCF_1}{(1+R)^1}+\frac{FCF_2}{(1+R)^2}+...+\frac{FCF_t+TV_t}{(1+R)^t}$
			- where 
			- $TV_t = \frac{FCF_{t+1}}{R-g}=\frac{FCF_{t}(1+g)}{R-g}$ 
			- $FCF = (Sales-Total\ costs)\times(1-T_C)-Net\ investment$
			- $Net\ investment = \Delta NWC+Capital\ spending-Depretiation$