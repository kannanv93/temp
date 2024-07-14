# temp
Development team applied numerous transformations to test the stationarity of transformed dependent variables and their trend with historical macroeconomic variables. Various transformations applied on PD data to derive independent variables. All the transformed dependent variables were tested for stationarity with KPSS, ADF, and PP tests and passing any of these tests were used a basic-criteria to shortlist the dependent variable for modeling. The team has downloaded forecast of 19 macroeconomic variables from economy.com. Macroeconomic data is available from 1950Q2 to 2052Q4 at quarterly level

It is important to note that the model development team adopt a more relaxed approach in these new models in terms of satisfying the statistical assumption of these individual variables, rather, model performances are evaluated as a whole. For example, instead of focusing on the stationary of individual independent or dependent variables, the model development team still considered all the variables in the pool of prospective variables to use and focused on the stationarity/ linearity of the resulting models. The reason for adopting this methodology is that most of the variables and their transformations are not stationary as the development data contains only one credit cycle. However, if logically seen, over a longer horizon, the variables like default rates become stationary anyways.

The following is a summary of the data transformations that the Bank systematically applied to its dataset:
Supervisory macroeconomic variables (X):
	level (no transformation applied)
	logarithm (log) transformation
	quarter-over-quarter difference or quarter-over-quarter growth
	year-over-year difference or year-over-year growth
	quarter-over-quarter log growth
	year-over-year log growth
	up to 6 quarter lags (n= 1 to 6)

Quarter-over-Quarter difference
Applied MEV Group: interest rate sector or rate-related MEVs (eg., unemployment rate)
Transformation Formula: MEV_q (t) = MEV(t) – MEV(t–1)
Make the data stationary

Year-over-Year difference
Applied MEV Group: interest rate sector or rate-related MEVs
Transformation Formula: MEV_y (t) = MEV(t) – MEV(t–4)
Make the data stationary and remove seasonal component

Quarter-over-Quarter growth
Applied MEV Group: all MEVs other than interest rate sector or rate-related MEVs
Transformation Formula: MEV_q (t)=MEV(t)/MEV(t–1)   – 1

Year-over-Year growth
Applied MEV Group: all MEVs other than interest rate sector or rate-related MEVs
Transformation Formula: MEV_y (t)=MEV(t)/MEV(t–4) -1
Remove the level impact and growth rate of MEVs can extend the list of transformed MEVs

Quarter-over-Quarter log growth
Applied MEV Group: price or index related MEVs (e.g., Dow Jones stock index)
Transformation Formula: MEV_q log(t) = log(MEV(t)/MEV(t–1) )

Year-over-Year log growth
Applied MEV Group: price or index related MEVs
Transformation Formula: MEV_y log(t) = log(MEV(t)/MEV(t–4) )

Lag Quarter-over-Quarter log growth
Transformation Formula: MEV_q lag_log(t) = MEV_q log(t-1)

Lag Year-over-Year log growth
Transformation Formula: MEV_y lag_log(t) = MEV_y log(t-4)

Lag Quarter-over-Quarter difference
Transformation Formula: MEV_q lag(t) = MEV_q (t-1)
 
lag year-over-year difference
Transformation Formula: MEV_y lag(t) = MEV_y (t-4)

MA Quarter-over-Quarter Lag
Applied MEV Group: interest rate sector or rate-related MEVs (eg., unemployment rate)
Transformation Formula: MA_2_MEV_q (t) =MA_2_MEV(t–1) and MA_4_MEV_q (t) =MA_4_MEV(t–1)

MA Year-over-Year Lag
Transformation Formula: MA_2_MEV_y (t) =MA_2_MEV(t–4) and MA_4_MEV_y (t) =MA_4_MEV(t–4)

MA Quarter-over-Quarter difference
Transformation Formula: MA_2_MEV_q (t) =MA_2_MEV(t)-MA_2_MEV(t–1) and MA_4_MEV_q (t) =MA_4_MEV(t)-MA_4_MEV(t–1)



MA Year-over-Year difference
Applied MEV Group: interest rate sector or rate-related MEVs (eg., unemployment rate)
Transformation Formula: MA_2_MEV_y (t) =MA_2_MEV(t)-MA_2_MEV(t–4) and MA_4_MEV_y (t) =MA_4_MEV(t)-MA_4_MEV(t–4)

MA Quarter-over-Quarter Growth
Transformation Formula: MA_2_MEV_q (t)=(MA_2_MEV(t))/(MA_2_MEV(t–4))-1 and MA_4_MEV_q (t)=(MA_4_MEV(t))/(MA_4_MEV(t–4))-1

MA Year-over-Year Growth
Transformation Formula: MA_2_MEV_y (t)=(MA_2_MEV(t))/(MA_2_MEV(t–4))-1 and MA_4_MEV_y (t)=(MA_4_MEV(t))/(MA_4_MEV(t–4))-1

MA Quarter-over-Quarter log Growth
Transformation Formula: MA_2_MEV_q (t)=log⁡((M〖A_2〗_MEV(t) )/(M〖A_2〗_MEV(t–4)  )) and MA_4_MEV_q (t)=log((MA_4_MEV(t))/(MA_4_MEV(t–4)))

MA Year-over-Year log Growth
Transformation Formula: MA_2_MEV_y (t)=log((MA_2_MEV(t))/(MA_2_MEV(t–4))) and MA_4_MEV_y (t)=log((MA_4_MEV(t))/(MA_4_MEV(t–4)))
![image](https://github.com/user-attachments/assets/c00bc16f-575d-4b9b-8f99-b1802bd4c7cd)
