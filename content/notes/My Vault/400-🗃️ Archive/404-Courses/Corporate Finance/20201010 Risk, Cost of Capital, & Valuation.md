# [[20201010 Risk, Cost of Capital, & Valuation]]'
Notes: 
		[[001 Corporate Fin Class Notes]] 
tags: #literature-note #finance #corpfin 

### Topics/Key Concepts/Key Questions
1. Cost of equity
2. Estimation & determinants of beta
3. Cost of debt
4. Cost of preferred stock
5. Weighted average cost of capital (WACC)
6. Valuation with WACC
7. Flotation costs

### Learning Objectives
1. Calculate the beta of a common stock
2. Estimate the costs of equity, debt, and preferred stock for a firm
3. Compute the weighted average cost of capital 
4. Apply the WACC to determine the valuation of a firm
5. Describe the role of flotation costs in capital budgeting problems

### Lecture Notes
- Cost of Capital
	- The discount rate of a project should be the expected return on a financial asset of comparable risk
		- AKA required return or cost of capital
	- If all of a firm’s projects are equally risky, then the discount rate equals the cost of capital for the entire firm
- The Cost of Equity Capital
	- The required return on a stockholder’s investment in the firm
	- Used to discount the cash flows of new projects for **all-equity** firms
	- Estimated using the capital asset pricing model (CAPM)
		- $E(R_S) = R_F + \beta \times (R_M-R_F)$
		- $R_S = R_F + \beta \times (R_M-R_F)$

- Estimating the CAPM Parameters
- The ==Risk-Free Rate==
	- 1-year Treasury bill yield
	- Yield on a Treasury security with maturity that matches average maturity of project cash flows 
	- Government bond in local currency
- ==Market Risk Premium==
	- Historical risk premium
	- Estimate derived from dividend discount model (DDM):
		- $R_S = \frac{D_1}{P_0}+g$
- ==Beta== Estimation Techniques
	- Use the variance-covariance matrix
	 $$\beta_i = \frac{Cov(R_i,R_M)}{Var(R_M)}=\frac{\sigma_{i,M}}{\sigma^2_M}$$
	- Estimate a linear regression
		 $$R_i = \alpha_i + \beta_i R_M + e_i$$
	- Use the built-in Excel formula
		- = SLOPE(known ys, known xs)
- Problems with Beta Estimation Techniques
	- Betas tend to vary over time
	- The sample size may be inadequate
	- Betas are influenced by changing financial leverage and business risk
- Some argue that industry betas are more appropriate 
	- This should reduce estimation error
	- The operations of the firm must be similar to those of the rest of the industry
- Betas are determined by 3 major factors
	- The cyclicality of revenues
	- Operating leverage
	- Financial leverage
- Each project or division should be assigned a discount rate commensurate with its own risk
	- Try to focus on pure plays when calculating the average beta for the industry
	- New projects may necessitate an upward adjustment since they are often more responsive to market-wide movements
	- For a project that constitutes its own industry, find other firms with similar values for the three determinants of beta


- ==Cost of Debt==
	- Estimated based on the yield to maturity (YTM) for outstanding bonds
		- If there is no outstanding debt, then estimate using prospective rates
			- Seek guidance from investment banker about yield on prospective bonds 
			- Use the prospective borrowing rate for bank loans
	- Must account for the tax deductibility of interest payments
		- $After-tax\ cost\ of\ debt = (1-T_C) \times Borrowing\ rate$

- Cost of Preferred Stock
	- Estimated by rearranging the formula for the PV of a perpetuity
		- $R_P = \frac{D}{PV'}$
		- where
			- $R_P$ = yield (i.e., rate of return)
			- D = dividend
			- PV = present value (i.e., price)

- Weighted Average Cost of Capital
	- The return required on existing assets for the firm to maintain its value
	- Estimated as the weighted average cost of the firm’s equity and debt
		- $$WACC = \frac{S}{S+B} \times R_S + \frac{B}{S+B} \times R_B \times (1-T_C)$$
		- where
			- S = Market value of common stock
			- B = Market value of bonds
			- $R_S$ = Cost of equity
			- $R_B$ = Cost of debt
			- $T_C$ = Corporate tax rate
	- Can be modified to incorporate preferred stock financing
		- $$WACC = \frac{S}{S+B+P} \times R_S + \frac{B}{S+B+P} \times R_B \times (1-T_C) + \frac{P}{S+B+P} \times R_P$$
		- where
			- S = Market value of common stock
			- B = Market value of bonds
			- P = Market value of preferred stock
			- $R_S$ = Cost of equity
			- $R_B$ = Cost of debt
			- $R_P$ = Cost of preferred stock
			- $T_C$ = Corporate tax rate

- WACC reflects both the risk and capital structure of the firm’s existing assets
	- This renders it an appropriate discount rate when valuing the entire firm or a project of comparable risk
- To value a project, compute its NPV by discounting future cash flows at the WACC and subtracting the initial cost
	- $$NPV = -Initial\ cost+\sum^n_{t=1}\frac{CF_t}{(1+WACC)^t}=$$
	- $$-Initial\ cost+\frac{CF_1}{(1+WACC)^1}+\frac{CF_2}{(1+WACC)^2}+...+\frac{CF_n}{(1+WACC)^n}$$
- To value a firm, compute its NPV by discounting its net cash flows up to a horizon as well as its terminal value at the WACC 
	- $$PV_0=\frac{CFA^*_1}{(1+WACC)^1}+\frac{CFA^*_2}{(1+WACC)^2}+...+\frac{CFA^*_t+TV_t}{(1+WACC)^t}$$
	- where
		- $$TV_t = \frac{CF_{t+1}}{WACC-g_{CF}}=\frac{CF_t(1+g_{CF})}{WACC-g_{CF}}$$
		- $$CFA^*=EBIT-Taxes^*+Depreciation-Capital\ spending-\Delta NWC$$
		- Since incremental cash flows exclude financing costs, one must compute “adjusted” taxes that assume zero debt financing (i.e., $Taxes^*$ = EBIT * $T_C$)

- The terminal value can alternatively be estimated using the EV/EBITDA multiple for comparable firms
	- $$TC_{i,t}=\frac{EV_{comps}}{EBITDA_{comps}}\times EBITDA_{i,t}$$

- Flotation Costs
	- Expenses incurred when issuing stocks or bonds
	- Can be expressed as a weighted average using the target weights & flotation costs (as % of amount raised) for stocks and bonds
		- For internal equity, $f_s$ = 0%
		- $$f_A = \frac{S}{V} \times f_S + \frac{B}{V} \times f_B$$
	- Should be accounted for to capture the true cost of a project
		- $Necessary\ proceeds = (1-f_A)\times Amount\ raised$
		- Amount raised = $\frac{Necessary\ proceeds}{1-f_A}$













## Guiding Questions
1. How does one determine the appropriate discount rate when evaluating a project or valuing a firm?
2. What factors affect the costs of equity, debt, and preferred stock?
3. When calculating the WACC, should the weights of the various financing components be computed based on their relative book values or market values? Why?
4. How should flotation costs be accounted for in capital budgeting problems?