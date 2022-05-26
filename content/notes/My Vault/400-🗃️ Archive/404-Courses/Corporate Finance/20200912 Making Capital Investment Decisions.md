# [[20200912 Making Capital Investment Decisions]]

Notes: 
		[[001 Corporate Fin Class Notes]] 
tags: #literature-note #finance #corpfin 

#### Topics/Key Concepts/Key Questions
1. Measuring incremental cash flows
2. Alternative definitions of operating cash flow
3. Evaluating cost-cutting investments
4. Setting the bid price in competitive bidding
5. Using equivalent annual cost (EAC) to compare equipment with different lives 
6. Handling inflation in capital budgeting
#### Learning Objectives
1. determine the incremental cash flows for a capital investment
2. account for special considerations in capital budgeting, including after-tax salvage value, depreciation, and net working capital 
3. estimate operating cash flow using three different common approaches
4. evaluate special cases of discounted cash flow analysis, such as cost-cutting investments, competitive bidding, and comparisons of equipment with different lives
5. describe the implications of inflation in capital budgeting problems

#### Incremental Cash Flows
- Capital budgeting decisions should be based on cash flows, not earnings
- Only *incremental cash flows* are considered relevant
	- Focus on changes in the firm’s cash flows that occur as a direct consequence of accepting the project
	- **Include** the following:
		- Opportunity costs
		- Side effects 
		- Erosion 
		- Synergy
	- *Exclude* the following:
		- Sunk costs
		- Allocated costs
		- Financing costs
 
#### Computing Incremental Cash Flows
- Use **accounting data** from the tax books, not the stockholders’ books
- Incorporate the 2 major sources of cash flow
	1. Cash flow from operations (CFFO)
		- 𝐶𝐹𝐹𝑂 = 𝑆𝑎𝑙𝑒𝑠 𝑅𝑒𝑣𝑒𝑛𝑢𝑒 − 𝑂𝑝𝑒𝑟𝑎𝑡𝑖𝑛𝑔 𝐶𝑜𝑠𝑡𝑠 − 𝑇𝑎𝑥𝑒𝑠
		- do not subtract D&A because they are non-cash activities and do not affect CFs
	2. Total investment cash flow (TICF)
		- Acquisition and disposition of PP&E
			- Ignore interest expense from debt financing
		- Opportunity costs
		- Side effects
		- Investment in net working capital
- $$𝑇𝑜𝑡𝑎𝑙\ 𝐶𝑎𝑠ℎ\ 𝐹𝑙𝑜𝑤 = 𝐶𝐹𝐹𝑂+𝑇𝐼𝐶𝐹$$

#### After-Tax Salvage Value
- Represents cash flow from selling an asset
	- Captures tax effect when salvage value (i.e., market value) differs from adjusted basis (i.e., book value)
		- Salvage Value > Adjusted Basis  Tax paid on profit
		- Salvage Value < Adjusted Basis  Tax saved on loss
		- AT 𝑆𝑎𝑙𝑣𝑎𝑔𝑒 𝑉𝑎𝑙𝑢𝑒=𝑆𝑎𝑙𝑣𝑎𝑔𝑒 𝑉𝑎𝑙𝑢𝑒−𝑇_𝐶 (𝑆𝑎𝑙𝑣𝑎𝑔𝑒 𝑉𝑎𝑙𝑢𝑒−𝐴𝑑𝑗𝑢𝑠𝑡𝑒𝑑 𝐵𝑎𝑠𝑖𝑠) ,
		- 𝐴𝑑𝑗𝑢𝑠𝑡𝑒𝑑 𝐵𝑎𝑠𝑖𝑠=𝐼𝑛𝑖𝑡𝑖𝑎𝑙 𝐶𝑜𝑠𝑡 −𝐴𝑐𝑐𝑢𝑚𝑢𝑙𝑎𝑡𝑒𝑑 𝐷𝑒𝑝𝑟𝑒𝑐𝑖𝑎𝑡𝑖𝑜𝑛

#### Depreciation
- IRS Publication 946 outlines depreciation rules for tax purposes
	- Most property is depreciated based on the Modified Accelerated Cost Recovery System (MACRS) shown in Table 6.3
		- Recovery period class depends on property type 
		- Half-year convention
	$MACRS\ Depreciation=Initial\ Cost \times MACRS\ Depreciation\ \%$
	- Real property is depreciated on a straight-line basis
		$Straight-Line\ Depreciation = \frac{Initial\ Cost\ -\ Salvage\ Value}{Useful\ Life}$
		- Salvage value should be treated as 0 to depreciate an asset straight-line to 0
	- Tax Cut and Jobs Act (2017) allows 100% bonus depreciation for qualified property through 2023

#### Net Working Capital
$$NWC =  Current\ Assets - Current\ Liabilities$$
- Focus on cash, inventory, accts. receivable, & accts. payable
- Most projects require initial investment in NWC 
	- Purchase inventory
	- Provide a buffer against unforeseen expenditures
	- Allow for credit sales --> accounts receivable 
- Evolving NWC needs necessitate changes in NWC 
	- Positive (negative) Δ in NWC --> cash outflows (inflows)
$$Cash\ Flow\ for\ \Delta\ in\ NWC = Beginning\ NWC - Ending\ NWC$$
- NWC investment is usually recovered at end of project

### Project cash flows typically follow a common pattern
1. Cash outflow due to investment outlays at beginning of project
2. Cash inflows due to sales revenue over life of project
3. Final cash inflow due to sale of plant and equipment at end of project


### Alternative Definitions of ==Operating Cash Flow==
1. Top-Down Approach
	- $OCF = Sales - Cash\ costs - Taxes$
2. Bottom-Up Approach
	- Only valid when there is no interest expense
	- $OCF = Net\ income + Depreciation$
		- WHERE $Net\ income = EBT - Taxes$
	- $OCF = (Sales- Cash costs - Depreciation)(1-T_c)+Depreciation$
3. Tax Shield Approach 
	- $OCF = Sales - Cash\ costs - (Sales - Cash\ costs - Depreciation) \times T_c$
	- $OCF = (Sales - Cash\ costs)\times(1-T_c) + Depreciation \times T_c$
	- $OCF = Cost\ savings\ times (1-T_c)+Depreciation \times T_c$
	- $OCF = AT\ Cost\ Savings + Depreciation\ Tax\ Shield$

### Special Cases of Discounted Cash Flow (DCF) Analysis
1. Cost-cutting investments
2. Competitive bidding
3. Comparing equipment with different lives


### Competitive Bidding
- Must solve for unit price that makes NPV=0
	1. Construct a timeline of cash flows, including unknown OCF
	2. Modify the timeline after discounting all known future cash flows
	3. Solve for OCF that makes NPV=0
		- $NPV = 0 = PV\ of\ known\ cash\ flows + OCF \times PVIFA_{r,t}$
		- $PVIFA_{r,t}$ = present value interest factor for annuity of $1 per year for t years at discount rate of r
	4. Use OCF to solve for NI
		- $OCF = NI + Depreciation$
	5. Use NI to solve for sales, and then calculate unit price
		- **$NI = (Sales – Costs – Depreciation) \times (1 – T_C)$**

### Comparing Equipment with Different Lives
- Choose the investment with the lower equivalent annual cost (EAC)
	- Represents the value of the payment (C) in a fixed annuity with the same PV as the original set of cash flows
		- $PV\ of\ Costs = C \times PVIFA_{r,t}$
	- Underlying Assumptions:
		- Revenues are identical, but operating costs likely differ
		- Both investments can be replaced indefinitely
	- If assumptions are violated, use NPV analysis for mutually exclusive projects to account for both revenues and costs

### Inflation must be handled consistently in capital budgeting
- There are two acceptable approaches:
	1. Discount nominal cash flows at the nominal rate (R)
	2. Discount real cash flows at the real rate (r)
		- $𝑅𝑒𝑎𝑙\ 𝑖𝑛𝑡𝑒𝑟𝑒𝑠𝑡\ 𝑟𝑎𝑡𝑒= \frac{1+\ 𝑁𝑜𝑚𝑖𝑛𝑎𝑙\ 𝑖𝑛𝑡𝑒𝑟𝑒𝑠𝑡\ 𝑟𝑎𝑡𝑒}{1+𝐼𝑛𝑓𝑙𝑎𝑡𝑖𝑜𝑛\ 𝑟𝑎𝑡𝑒}−1$
		- $𝑅𝑒𝑎𝑙\ 𝑖𝑛𝑡𝑒𝑟𝑒𝑠𝑡\ 𝑟𝑎𝑡𝑒≈𝑁𝑜𝑚𝑖𝑛𝑎𝑙\ 𝑖𝑛𝑡𝑒𝑟𝑒𝑠𝑡\ 𝑟𝑎𝑡𝑒−𝐼𝑛𝑓𝑙𝑎𝑡𝑖𝑜𝑛\ 𝑟𝑎𝑡𝑒$
		- $𝑅𝑒𝑎𝑙\ 𝑐𝑎𝑠ℎ\ 𝑓𝑙𝑜𝑤 = \frac{𝑁𝑜𝑚𝑖𝑛𝑎𝑙\ 𝑐𝑎𝑠ℎ\ 𝑓𝑙𝑜𝑤}{(1+𝑖)^𝑡}$
- Both approaches yield the same NPV












