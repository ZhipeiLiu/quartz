# [[20200911 NPV & Other Investment Rules]]
Notes: 
		[[001 Corporate Fin Class Notes]] 
tags: #literature-note #finance #corpfin 


#### Key Concepts
1. Net present value (NPV)
2. Payback period
3. Discounted payback period
4. Internal rate of return (IRR)
5. Modified internal rate of return (MIRR)
6. Profitability index
7. Capital budgeting methods in practice
#### Learning Objectives
1. calculate common capital budgeting measures, including net present value, the payback period, the discounted payback period, the internal rate of return, and the profitability index
2. interpret the capital budgeting measures listed above
3. apply various investment decision rules to capital budgeting problems in order to determine whether a corporate project should be accepted or rejected
4. recognize the complications surrounding mutually exclusive investments and understand how to apply investment decision rules in order to choose between such competing investments
5. identify the major advantages and disadvantages of the primary investment decision rules

#### Net Present Value
Capital Budgeting
- Decision making process for accepting or rejecting projects
- Consider investment decision rules based on:
	1. ==NPV==
		- Sum of the PVs of future CFs - PV of the cost of the investment
		- CFs are discounted using an appropriate market interest rate
		- NPV > 0 | Accept
		--------- | ----------
		NPV < 0 | Reject
		- **Pros**
			- Accepting positive NPV projects benefits the stockholders
			- The value of the firm rises by the NPV of the project
			- The NPV rule uses the correct discount rate
		- NPV - **3 desirable attributes**
			- based on cash flows
			- uses all the cash flows of the project
			- discounts the cash flows properly
	2. ==Payback Period==
		- the amount of time required to recover the inital cost of an investment
		- Payback Period <= Predetermined length of time | Accept
		--------- | ----------
		Payback Period > Predetermined length of time | Reject
		- $$Payback\ Period = \#\ Full\ Years + \frac{Initial\ Investment - Cumulative\ CF\ for\ Last\ Full\ Year}{CF\ for\ Next\ Year}$$
		- **Disadvantages**
			- Ignores the timing of CFs within the payback period
			- Ignores payments after the payback period
			- The choice of the payback cutoff date is arbitrary
			- It is biased against long-term projects
			- It may result in the firm accpeting a negative-NPV project
		- **Advantages**
			- Simplicity - appealing for minor investment decisions
			- Its focus on quick cash recovery increases resinvestment possibilities for capital-constrained firms with ample growth opportunities
			- Managers' decision making ability can be evaluated relatively easily
	3. ==Discounted Payback Period==
		- The amount of time required for a project's discounted CFs to equal its initial investment
		- Discounted Payback Period <= Predetermined length of time | Accept
		--------- | ----------
		Discounted Payback Period > Predetermined length of time | Reject
		- $$Discounted\ Payback\ Period = \#\ Full\ Years + \frac{Initial\ Investment - Cumulative\ PV\ of\ CF\ for\ Last\ Full\ Year}{PV\ of\ CF\ for\ Next\ Year}$$
		- **Problems**
			- It ignores payments after the payback period
			- The choice of the discounted payback cutoff date is arbitrary
			- It is biased against long-term projects
	4. ==Internal Rate of Return (IRR)==
		- The discount rate at which the NPV of an investment is zero
		- summarizes a potentially complex project using a single, internally generated rate of return
		- $$NPV = CF_0 + \frac{CF_1}{(1+MIRR)} + \frac{CF_2}{(1+MIRR)^{2}}...$$
		- IRR > Discount Rate | Accept
		--------- | ----------
		IRR < Discount Rate | Reject
		- Certain situations necessitate modifications
			- Financing type projects
			- Projects with multiple CF sign changes
			- Mutually exclusive projects
		- **Disadvantages** of the IRR Method
			1. The decision rule depends on the nature of the project
				- **Investing type project**
					- Cash outflow *preceding* cash inflows
					- IRR > Discount Rate | Accept
					--------- | ----------
					IRR < Discount Rate | Reject
				- **Financing type project**
					- Cash outflow *following* cash inflows
					- IRR > Discount Rate | Accept
					--------- | ----------
					IRR < Discount Rate | Reject
			2. There may be **multiple IRRs** whne the cash flows exhibit multiple changes in sign
				- problem: could be multiple IRRs
				- solution: modify the CFs and compute for MIRR - modifies the CFs so that there is only one change in sign
			3. It ignores **scaling issues** when comparing mutually exclusive projects - AKA scale problem
				- 3 Approaches to Mutually Exclusive Investments
					1. Compare the NPVs of the choices
					2. Calculate the **incremental NPV**
					3. Compare the **incremental IRR** (based on incremental NPV) to the discount rate
			4. It also ignores **timing differences** between the cash flows of mutually exclusive projects - AKA timing problem
				1. Compare the NPVs of the choices
				2. Calculate the **incremental NPV**
				3. Compare the **incremental IRR** (based on incremental NPV) to the discount rate
	1. ==IRR for Projects with Irregular CFs==
		- Use XIRR in excel
		- XIRR(date_range,CF_range)
	2. ==Modified Internal Rate of Return (MIRR)==
		- MIRR > Discount Rate | Accept 
		--------- | ----------
		MIRR < Discount Rate | Reject
		- Excel's built-in MIRR(CFs, disc rate, reinvestment rate) - corresponds to the #3 method
		- Method #1 - **The Discounting Approach**
			- Discount all *negative* cash flows back to the present and add them to the initial cost
		- Method #2: **The Reinvestment Approach**
			- Compound all cash flows (except the first) to the end of the project’s life
			- Compute IRR using modified cash flows
		- Method #3: **The Combination Approach**
			- Discount all negative cash flows back to the present and add them to the initial cost
			- Compound all positive cash flows to the end of the project’s life
			- Compute IRR using modified cash flows
		- **Advantages** of MIRR
			- the approach yields a single rate of return
		- **Disadvantages** of MIRR 
			- Lack of a single established method of computation
			- Interpretation complications due to use of modified cash flows
			- Reliance on externally supplied discount or compounding rate
		- Cash Flows | # IRRs | IRR Criterion | NPV Criterion
		--------- | --------- | --------- | --------- 
		1st cash flow is negative and all remaining cash flows are positive | 1 | Accept if IRR > r; Reject if IRR < r | Accept if NPV > 0; Reject if NPV < 0
		1st cash flow is positive and all remaining cash flows are negative | 1 | Accept if IRR < r; Reject if IRR > r | Accept if NPV > 0; Reject if NPV < 0
		Some cash flows after 1st are positive and others are negative | Possibly more than 1 | No valid IRR | Accept if NPV > 0; Reject if NPV < 0
	7. ==Profitability Index==
		- $$PI = \frac{PV\ of\ CFs\ subsequent\ to\ initial\ investment}{Initial\ investment}$$
		- PI > 1  | Accept 
		--------- | ----------
		PI > 1 | Reject
		- Modifications are sometimes necessary
			- Mutually exclusive projects
			- Capital rationing