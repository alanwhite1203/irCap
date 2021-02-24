# A Description of Interest Rate Caps and Floors Valuation

	Overview
An interest rate cap is an OTC derivative where the buyer receives payments at the end of each period when the interest rate exceeds the strike, whereas an interest rate floor is a similar contract where the buyer receives payments at the end of each period when the interest rate is below the strike. Caps and floors are widely used to hedge against interest rate fluctuations. 
An interest rate cap is a financial contract between two parties that provides an interest rate ceiling or cap on the floating rate payments. It actually consists of a series of European call options (caplets) on interest rates.  The buyer receives payments at the end of each period when the interest rate exceeds the strike.  In return, the buyer needs to pay an up-front premium to the seller.
Interest rate caps are frequently purchased by issuers of floating rate debt who wish to protect themselves from the increased financing costs that would result from a rise in interest rates. Investors use caps to hedge against the risk associated with floating interest rate and will benefit from any risk in interest rates above the strike. The holder gets a payment when the underlying interest rate exceeds a specified strike rate. This presentation gives an overview of interest rate cap products and valuation model. 

Keywords
Interest rate cap, interest rate floor, caplet, floorlet, call option, put option, valuation, Black model

	Interest Rate Cap Introduction
	An interest rate cap is a financial contract between two parties that provides an interest rate ceiling or cap on the floating rate payments.
	An interest rate cap actually consists of a series of European call options (caplets) on interest rates. 
	The buyer receives payments at the end of each period when the interest rate exceeds the strike.  The payment frequency could be monthly, quarterly or semiannually.
	The exercise is done automatically that is different from any types of options.
	For example, let the strike be 2.0%. The buyer would get paid if LIBOR rose above 2.0%; otherwise, he would receive nothing if LIBOR fell below it.
	The buyer needs to pay an up-front premium to the seller.

	The Benefits of a Cap
	Caps are frequently purchased by issuers of floating rate debt who wish to protect themselves from the increased financing costs that would result from a rise in interest rates.
	Investors use caps to hedge against the risk associated with floating interest rate.
	Investors will benefit from any risk in interest rates above the strike.
	The holder gets a payment when the underlying interest rate exceeds a specified strike rate.

	The Payoff of a Caplet
	The payoff of a caplet
Payoff=N*τ*max(R-K,0)
where N – the notional; R – the realized interest rate; K – the strike; τ – the day count fraction.
	Payoff diagram
 

	Valuation
	The present value of a cap is given by
PV(0)=N∑_(i=1)^n▒〖τ_i D_i (F_i Φ(d_1 )-KΦ(d_2)) 〗
where 
D_i=D(0,T_i) – the discount factor; 
F_i=F(t;T_(i-1),T_i )=(D_(i-1)/D_i -1)/τ_i – the forward rate for period (T_(i-1),T_i).
Φ – the accumulative normal distribution function
d_1,2=(ln⁡(F_i/K)±0.5σ_i^2 T_i)/(σ_i √(T_i ))

	Practical Notes
	Interest rate caps are valued via the Black model in the market.
	The forward rate is simply compounded.
	The first key to value a cap is to generate the cash flows. The cash flow generation is based on the start time, end time and payment frequency, plus calendar (holidays), business convention (e.g., modified following, following, etc.) and whether sticky month end.
	Then you need to construct interest zero rate curve by bootstrapping the most liquid interest rate instruments in the market. The most common used yield curve is continuously compounded.
	Another key for accurately pricing an outstanding cap/floor is to construct an arbitrage-free volatility surface. 
	The accrual period is calculated according to the start date and end date of a cash flow plus day count convention
	The formula above doesn’t contain the last live reset cash flow whose reset date is less than valuation date but payment date is greater than valuation date. The reset value is 
〖PV〗_reset=N*τ*max(R-K,0)

   which should be added into the above present value.

	A Real World Example
Buy Sell	Sell
Strike	0.035
Trade Date	1/11/2016
Start Date	1/13/2016
Maturity Date	1/2/2019
Currency	USD
Day Count	dcAct360
Rate type	Float
Notional	15090000
Pay Receive	Pay
Payment Frequency	1M
Index Tenor	1M
Index Type	LIBOR


Reference:
https://finpricing.com/knowledge.html

