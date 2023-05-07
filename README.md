Download Link: https://assignmentchef.com/product/solved-fe621-homework-2
<br>
<strong>Problem 1 . The Binomial Tree.</strong>

<ul>

 <li>Construct code to calculate option values using <em>an additive binomial tree</em>. For this part you need four versions: European and American as well as Call and Put. You <em>may </em>use the same tree construction (and function) for all options.</li>

 <li>Download Option prices (you can use the Bloomberg Terminal, Yahoo! Finance, etc.) for an equity, for 3 different maturities (1 month, 2 months, and 3 months) and 20 strike prices close to the value at the money. If 3 months does not exist use next one available. Please download the data DURING THE TRADING DAY (9:00am to 4:30pm ET). Otherwise your values will be way off. Do not forget to download the value of the underlying. For each strike price in the data, use the implied vol values in Homework 1 (see Problem 1c) and the current short-term interest rate (the Feds Fund rate is a good choice). Calculate the option price (European Calls and Puts) using the binomial tree, and compare the results with the Black–Scholes price. Use at least 200 steps in your tree construction. Treat the options as American as well and plot these values side by side with the European and Black Scholes values. When you create the plot do not forget to plot the bid-ask values as well. If you downloaded DATA 2 for last assignment you can use that as your data set.</li>

 <li>Comment of the table in the previous part.</li>

 <li>Consider <em>N </em>∈{10<em>,</em>20<em>,</em>30<em>,</em>40<em>,</em>50<em>,</em>100<em>,</em>150<em>,</em>200<em>,</em>250<em>,</em>300<em>,</em>350<em>,</em>400}. Compute and plot the absolute error for the European Put <em>ε<sub>N </sub></em>for as a function of</li>

</ul>

<em>N </em>∈N<sup>∗ </sup>the number of steps in the tree:

<em>,</em>

where <em>P<sup>BSM</sup></em>(<em>S</em><sub>0</sub><em>,K,T,r</em>;<em>σ</em>) and <em>P<sub>N</sub><sup>BinomTree</sup></em>(<em>S</em><sub>0</sub><em>,K,T,r</em>;<em>σ</em>) are the Black– Scholes–Merton price and the price calculated using a binomial tree with <em>N </em>steps, respectively. What do you observe?

<strong>Problem 2 . Pricing Exotic Options using Trinomial Trees. </strong>We will use here a synthetic example to illustrate using trees to price path dependent options. Please read Section 2.10 in [1] and Sections 1 and 5.1 in [2] (available <a href="https://www.math.kth.se/matstat/seminarier/reports/K-exjobb09/090601a.pdf">here</a><a href="https://www.math.kth.se/matstat/seminarier/reports/K-exjobb09/090601a.pdf">)</a>, and solve the following problems.

<ol>

 <li>Construct a trinomial tree to calculate the price of an European Up-and-Out call option. Use <em>S</em><sub>0 </sub>= 10, strike <em>K </em>= 10, maturity <em>T </em>= 0<em>.</em>3, volatility <em>σ </em>= 0<em>.</em>2, short rate <em>r </em>= 0<em>.</em>01, dividends <em>δ </em>= 0 and barrier <em>H </em>= 11. See Chapter 3 in [1] for the trinomial tree construction. Use as many steps in your tree as you think are necessary. For the option pricing you may consult the algorithm in the book [1] and try and figure out how to modify the code there to work with the new option and the new tree. Note the book details the computation using a binomial tree while we ask you to use a trinomial tree here.</li>

 <li>For the European Up-and-Out Call option explicit formulas exist. For example, implement the formula (5.2) from [2] and compare your results with part (a). Use the same parameters as before. Are your results matching? Note the paper is uploaded to the course shell under the name “Pricing Barrier Options”.</li>

 <li>Price an European Up-and-In call option, using the same parameters as before. Two methods can be employed: the analytical solution in (5.1) or the In-Out parity. Use both methods in order to verify your results.</li>

 <li>Calculate the price of an AMERICAN Up and In Put option</li>

</ol>

<strong>Problem 3 . Effects of dividend assumptions</strong>

To compute prices of a 6 -month American call option, future prices of the underlying stock are modeled with a 2 -period binomial tree with 3 month periods. You are given: (i) In each period, the price of the stock are either multiplied by 1.2 or multiplied by 0.9 (ii) The initial stock price is 40 . (iii) The continuously compounded risk-free interest rate is 4%.

<ol>

 <li>If the stock pays continuous dividends proportional to its price, and the dividend yield is 2%, then determine the range of possible strike prices for which early exercise is optimal. <em>Hint</em>: discuss all possible situations for the strike prices.</li>

 <li>If the stock pays one-time discrete dividends at 3 months time, and the dividend payment is proportional to the corresponding stock price with the proportion being 3%, then determine the range of possible strike prices for which early exercise is optimal.</li>

</ol>

<strong>Bonus Problem 1. A two-dimensional tree for the Heston model. </strong>Beliaeva and Nawalkha (2010) have developed in [7] a path-independent two-dimensional tree for the Heston model. In their approach, separate trees for the stock price and for the variance are constructed independently of one another, and then recombined, please see Chapter 8 in [5] for a detailed presentation.

<ul>

 <li>Price an American Put Option using the Beliaeva and Nawalkha method. Please note that the code provided in the book is incomplete (marked with ”<em>…</em>”). Consider the same numerical values for the parameters of interest as in [6].</li>

 <li>Price an European Call Option using the Beliaeva and Nawalkha method. Compare this result with the prices obtained in Homework 1, Problem 3 via the analytical formula. Consider the same numerical values as in [6]. What can you observe?</li>

</ul>

<strong>Bonus Problem 2 (30 points). Pricing variance swaps using trinomial trees. </strong>In the paper [8] the authors demonstrate how approximate the price of Variance Swaps using trees. THe model they demonstrate pricing is a stochastic volatility model as it makes little sense to price variance and volatility derivatives in models where the volatility is constant. However, in this bonus problem we will perform this nonsensical approach. Specifically, first construct the trinomial tree in Problem 2. We will use this tree with the same parameters: Use <em>S</em><sub>0 </sub>= 10, strike <em>K </em>= 10, maturity <em>T </em>= 0<em>.</em>3, volatility <em>σ </em>= 0<em>.</em>2, short rate <em>r </em>= 0<em>.</em>01, dividends <em>δ </em>= 0 to price a variance swap calculated using log returns. To do this please read the paper. You will need to implement the appropriate function <em>g </em>in formula (15). Please price a 60 day variance swap using a 60 steps tree (i.e., <em>n </em>= 60 and <em>l </em>= 1). The calculation is detailed in formulas (16).

<h1>References</h1>

<ul>

 <li>Clewlow, Les and Strickland, Chris. <em>Implementing Derivative Models (Wiley Series in Financial Engineering)</em>, John Wiley and Sons 1996.</li>

 <li>Niklas Westermark. <em>Barrier Option Pricing</em>, Degree Project in Mathematics, First Level. KTH Royal Institute of Technology, Stockholm, Sweden.</li>

 <li>Pooley, D. M., Vetzal, K. R., and Forsyth, P. A., <em>Convergence remedies for non-smooth payoffs in option pricing.</em>. Journal of Computational Finance, Vol. 6, No. 4, 2003.</li>

 <li>Florescu, Ionu¸t, Viens, Frederi G, <em>Stochastic volatility: option pricing using a multinomial recombining tree</em>, Applied Mathematical Finance, Vol. 15, No. 2, pp. 151–181, 2008, Taylor &amp; Francis.</li>

 <li>Rouah, F. D. <em>The Heston Model and Its Extensions in Matlab and C</em>, 2013, John Wiley and Sons.</li>

 <li>Mikhailov, Sergei and N¨ogel, Ulrich. <em>Heston’s stochastic volatility model: Implementation, calibration and some extensions </em>2004, John Wiley and Sons.</li>

 <li>Beliaeva, Natalia A and Sanjay K, Nawalkha, <em>A simple approach to pricing American options under the Heston stochastic volatility model</em>. The Journal of Derivatives, Vol. 17, No. 4, pp. 25–43, 2010.</li>

 <li>Zhao, Honglei and Zhao, Zhe and Chatterjee, Rupak and Lonon, Thomas and Florescu, Ionu¸t <em>Pricing variance, gamma, and corridor swaps using multinomial trees</em>. The Journal of Derivatives, Vol. 25, No. 2, pp. 7–21, 2017.</li>

</ul>