# [[20201109 Valuation & Capital Budgeting for the Levered Firm]]

Notes: 
		[[001 Corporate Fin Class Notes]] 
tags: #literature-note #finance #corpfin 

### Valuation methods for levered firms
1. Adjusted present value (APV) approach
2. Flow to equity (FTE) approach
3. Weighted average cost of capital (WACC) approach

### The APV Method 
- Computes the value of a project to a levered firm as the sum of 2 components:
	- The value of the project to an unlevered firm (NPV)
	- The net present value of the financing side effects (NPVF)
		- The tax subsidy to debt (TCB for perpetual debt)
		- The costs of issuing new securities
		- The costs of financial distress
		- Subsidies to debt financing
	- $$APV = NPV+NPVF=\sum^\infty_{t=1} \frac{UCF_t}{(1+R_0)^t}-Initial\ Investment + NPVF$$
- Additional Considerations
	- The APV approach can also be used to value an entire levered firm as the sum of 2 components:
	- The value of the firm under all-equity financing (NPV)
	- The net present value of the financing side effects (NPVF)
	- The depreciation tax shield is often discounted using RF or a slightly higher rate (e.g., $R_B$)
	- The NPV of the financing side effects can be captured by the NPV of the loan’s after-tax cash flows
		- Discount cash flows using $R_B$
		- Formula ignoring flotation costs:
			- 𝑁𝑃𝑉_𝑙𝑜𝑎𝑛=𝐺𝑟𝑜𝑠𝑠 𝑝𝑟𝑜𝑐𝑒𝑒𝑑𝑠−𝑃𝑉(𝐴𝑇 𝐼𝑛𝑡𝑒𝑟𝑒𝑠𝑡 𝑝𝑎𝑦𝑚𝑒𝑛𝑡𝑠)−𝑃𝑉(𝐿𝑜𝑎𝑛 𝑟𝑒𝑝𝑎𝑦𝑚𝑒𝑛𝑡𝑠)
		- Formula including flotation costs:
			- 𝑁𝑃𝑉_𝑙𝑜𝑎𝑛=𝑁𝑒𝑡 𝑝𝑟𝑜𝑐𝑒𝑒𝑑𝑠−𝑃𝑉(𝐴𝑇 𝐼𝑛𝑡𝑒𝑟𝑒𝑠𝑡 𝑝𝑎𝑦𝑚𝑒𝑛𝑡𝑠) - 𝑃𝑉(𝐿𝑜𝑎𝑛 𝑟𝑒𝑝𝑎𝑦𝑚𝑒𝑛𝑡𝑠)+𝑃𝑉(𝐹𝐶 𝑇𝑎𝑥 𝑠ℎ𝑖𝑒𝑙𝑑)

### The FTE Method 
- Estimates the value of a project by discounting its cash flows to the equity holders of the levered firm at the cost of levered equity capital
- Involves a 3-step process
	1. Calculate the levered cash flows (LCFs)
	2. Calculate the discount rate (RS)
	3. Value the project
	- $$NPV=\sum^\infty_{t=1} \frac{LCF_t}{(1+R_S)^t}-(Initial\ Investment - Amount\ borrowed)$$
	- Discount the levered cash flows at the cost of levered equity capital
		- $$NPV=\sum^\infty_{t=1}\frac{LCF_t}{(1+R_S)^t}$$

### WACC Method
- Used to value a project or firm by discounting unlevered cash flows at the WACC using target weights
	- $WACC=\frac{S}{S+B} \times R_S + \frac{B}{S+B}\times R_B\times(1-T_C)$
	- Formula for Project Valuation
		- $$NPV=\sum^\infty_{t=1}\frac{UCF_t}{(1+WACC)^t}-Initial\ Investment$$
	- Formula for Firm Valuation
		- $$NPV=\sum^\infty_{t=1}\frac{UCF_t}{(1+WACC)^t}$$

### Guidelines for Selecting Among the Methods
- Use FTE or WACC if the firm’s target debt-value ratio is fixed over the project’s life
- Use APV if the project’s level of debt is known over the project’s life

### Beta and leverage
- Types of Betas
	- Levered beta (AKA equity beta)
	- Unlevered beta (AKA asset beta)
- The Effect of Leverage on the Equity Beta Without Taxes
	- Assumes the beta of debt is 0
	- $$\beta_{𝐸𝑞𝑢𝑖𝑡𝑦}=\beta_{𝐴𝑠𝑠𝑒𝑡}\times(1+\frac{𝐷𝑒𝑏𝑡}{𝐸𝑞𝑢𝑖𝑡𝑦})$$
- The Effect of Leverage on the Equity Beta With Taxes
	- Assumes the beta of debt is 0
	- $$\beta_{𝐸𝑞𝑢𝑖𝑡𝑦} = (1+\frac{(1−𝑇_𝐶)\times 𝐷𝑒𝑏𝑡}{𝐸𝑞𝑢𝑖𝑡𝑦})\times \beta_{𝑈𝑛𝑙𝑒𝑣𝑒𝑟𝑒𝑑\ 𝑓𝑖𝑟𝑚}$$
- Unlevering the Equity Beta
	- $$\beta_{𝑈𝑛𝑙𝑒𝑣𝑒𝑟𝑒𝑑\ 𝑓𝑖𝑟𝑚}=\frac{\beta_{𝐸𝑞𝑢𝑖𝑡𝑦}}{[1+\frac{(1−𝑇_𝐶)\times 𝐷𝑒𝑏𝑡}{𝐸𝑞𝑢𝑖𝑡𝑦}]}=$$
	- $$= \frac{𝐸𝑞𝑢𝑖𝑡𝑦}{𝐸𝑞𝑢𝑖𝑡𝑦+(1−𝑇_𝐶)\times 𝐷𝑒𝑏𝑡 }\times \beta_{𝐸𝑞𝑢𝑖𝑡𝑦}$$
- If a project is not scale-enhancing, then the discount rate can be estimated based on the average unlevered beta in the industry
	1. Unlever the betas of comparable firms in the industry
	2. Calculate the average unlevered beta in the industry
	3. Relever the beta using the D/E ratio for the project
	4. Calculate the cost of levered equity using the CAPM
	5. Calculate the WACC
	6. Calculate the project’s NPV
