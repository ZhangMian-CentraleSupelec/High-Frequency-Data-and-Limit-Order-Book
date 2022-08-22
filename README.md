# High Frequency Data and Limit Order Book
- This is basically based on the course of High-frequency data and limit order book in CentraleSupelec. 
- It will be divided into 6 parts.
- Deal to the non-disclosure agreement, the disclosure of data is strictly forbiddened.


### What we have reached

Hawkes model is a good fit for limit order book.

![image](https://user-images.githubusercontent.com/110284601/185869172-4f6eb2f5-b44b-4e19-95a5-d07d4de8ce21.png)







# SUMMARY

## Part1. The Introduction to the High Frequency Data
  - Overview of the data
  - Trade duration
  - Trade volume
  - Intraday activity
  - High-frequency log returns and trading activity
## Part2. The Limit Order Book
  - Multiple prices
  - Spread distribution
  - Imbalance and trading activity
  - Autocorrelation of trade signs
  - Average shape of the Limit Order Book
 ## Part3. Point Process - Poisson Process
  - Time homogeneous Poisson Process
  - Non-time homogeneous Poisson Process for trades
 ## Part4. Point Process - Hawkes Process
  - The basic peoperties of Hawkes Process
  - Test the goodness of fit for the Hawkes Process
  - Simulation of Hawkes Process on MLE
 ## Part5. Hawkes Process in Finance
  - The fit of Hawkes Model to the limit order book
  - Systematic analysis.
 ## Part6. Poisson Process and Limit Order Book - Perfect Market Making
  - Sanity check
  - Simulation of limit order book

# PRESENTATION RESULT
  ## Part1. The Introduction to the High Frequency Data
  - The overview of the data 

  This is the trading volume of the stock which start from 2017-01-02.
  
  ![image](https://user-images.githubusercontent.com/110284601/184824673-22d4ee5e-0926-4218-9de3-2701d16c49ad.png)
  
  - Trade duration and the fit

  Here is the histogram of the trading volume, and most of the was traded in a very short instant. And here is the exponential fit of the histogram. Because the limit book can be considered as a poisson process and the exponential fit seems quite make sense. We use the traditional fit and the log-scale fit, the weibull fit and also the powerlow fit. We could find that in the tail, the weibull is the best fit.
  
  ![image](https://user-images.githubusercontent.com/110284601/184825187-94fea6ac-7bad-4726-adcd-a9090f2feeb2.png)
  ![image](https://user-images.githubusercontent.com/110284601/184825530-67dfed03-b504-482f-b85f-245c6ae9a98c.png)
  ![image](https://user-images.githubusercontent.com/110284601/184826290-c5f716df-510e-464f-adbd-3c35f6da9690.png)
  
  - Trading volume
  
  Here we present the log-fit of the histogram of the trading volume and also the powerlaw fit.
  
  ![image](https://user-images.githubusercontent.com/110284601/184826735-a593e93f-65f1-4e23-adcf-f9ceadfd5e91.png)
  ![image](https://user-images.githubusercontent.com/110284601/184826756-395177cb-9fd8-4e7d-8405-159c3f21bbf8.png)
  
  - Intraday activity

  The trading volume within a day.
  
  ![image](https://user-images.githubusercontent.com/110284601/184826811-52f430b5-9bcd-4d75-b8be-76d9c53783fc.png)
  
  - High-frequency log returns and trading activity

  The trading activity and the log-return is highly correlated.
  
  ![image](https://user-images.githubusercontent.com/110284601/184827240-0e654210-2f0d-4951-b6f7-72ad7f395ed4.png)
  ![image](https://user-images.githubusercontent.com/110284601/184827076-785476f4-1ef2-4732-87b4-dfdab9c06567.png)
  
  ## Part2. The Limit Order Book
  - The bid-ask analysis
  
  Here we calculate the best ask / best bid price of the stock and calculate the mid-price, compared with the real price.
  
  ![image](https://user-images.githubusercontent.com/110284601/184833242-6e26632d-cfce-4876-a240-3bce1656901f.png)
  
  - The distribution of bid-ask spread
  
  It is noticeable that the histogram in event time the most common spread (by a significant margin) is 0.01 (two ticks) whereas in calendar time, it is 0.005 (one tick), which means that events where the spread is two ticks are fixed quickly.
  
  ![image](https://user-images.githubusercontent.com/110284601/184833596-cae2c10a-21c1-431e-81a1-2a43c0869840.png)
  ![image](https://user-images.githubusercontent.com/110284601/184833666-15981b6e-f1d7-47f6-befe-0ee5b7d938ed.png)
  
  - The imbalance of the bid-ask spread
  
  Here we plot the relationship between the imbalance of the bid-ask spread and the pricing movement.
  
  ![image](https://user-images.githubusercontent.com/110284601/184834297-09664168-8a1d-4c0d-b058-b2a804a6c40c.png)
  ![image](https://user-images.githubusercontent.com/110284601/184834335-538d9237-b4b6-48b6-b287-d8e017f64bc3.png)
  ![image](https://user-images.githubusercontent.com/110284601/184834418-e6077006-ccf0-4172-bf18-97c339d29c8c.png)
  
  - Autocorrelation of trade signs
  
  The autocorrelation of trade signes decreases slowly as a function of the lag. It means that the trades are not independant from each others.
  
  ![image](https://user-images.githubusercontent.com/110284601/184834578-d8b5deca-1d6f-4ed9-884e-ffd56d4f30e7.png)
  
  - Average shape of the LOB
  
  Here we compared the trading time and calender time, the distrubution is quite similar.
  
  ![image](https://user-images.githubusercontent.com/110284601/184834665-87073053-2a33-4c35-9cfa-51fe372cbbc0.png)
  ![image](https://user-images.githubusercontent.com/110284601/184834725-59e70498-b090-411d-b940-35f01195ea00.png)
  
  ## Part3. Point Process - Poisson Process
  
  - Time homogeneous Poisson Process

  Here we fit the intensity of the poisson process with respect to the empirical intensity.
  
  ![image](https://user-images.githubusercontent.com/110284601/184835362-3c37c9ab-82bb-44c2-b086-99b266e6f697.png)
  ![image](https://user-images.githubusercontent.com/110284601/184835374-c1d953bd-dac3-4f85-94c1-a00c5f17e04e.png)

  ![image](https://user-images.githubusercontent.com/110284601/184835548-6cea8b75-1736-4085-8773-e53308ad815d.png)
  
  The above plot allows us to check that the simulation ran correctly, as it shows an higher trading intensity in the morning and in the evening (steeper slopes in the cumulated number of trades) aligned with the higher regions in the measured intensity.

  - Non-time homogeneous Poisson Process for trades
  
  ![image](https://user-images.githubusercontent.com/110284601/184835675-98723e9d-459d-4858-ab3c-a9f8ecb3b1ba.png)

  The simulated distribution has a less heavy tail than the empirical one. The non-homogeneous Poisson process is not a good fit for trades' durations.

  ## Part4. Point Process - Hawkes Process
  
  - The basic peoperties of Hawkes Process 
  
  Here we define the function of simulation Hawkes Process.
  
  ```
  def simulate_hawkes(alpha,beta,lambda_0,T):
    t = 0
    lstar = lambda_0
    events = []
    sum_nu = 0
    while t<T:
        u = np.random.random()
        t = t-np.log(u)/lstar
        lambda_t = lambda_0+np.exp(-beta*t)*sum_nu
        if t>=T:
            return events
        d = np.random.random()
        if d < lambda_t/lstar:
            lstar = lambda_t + alpha
            sum_nu += alpha*np.exp(beta*t)
            events += [t]
        else:
            lstar = lambda_t       
  ```

  - Test the goodness of fit for the Hawkes Process
  
  ![image](https://user-images.githubusercontent.com/110284601/184836231-796b4e53-417b-481b-b12a-e347d406a7a6.png)
  
  We find that the transformed durations are distributed according to an exponential with parameter 1, which indicates a good fit.

  - Simulation of Hawkes Process on MLE 
  
  As we have 3 parameters to estimate, we expect $\frac{1}{det(cov(\theta^*-\hat{\theta}_T))}$ to be linear in $T^{3 }$, which appears to be the case.
  
  ![image](https://user-images.githubusercontent.com/110284601/184840500-bc0fa84b-bc50-43d2-afcf-7936b9fba139.png)
  ![image](https://user-images.githubusercontent.com/110284601/184840529-4650fbc2-6cf7-4620-a6c8-a4da4dfac712.png)
  
  Parameter estimation time seems linear in 𝑇 , simulation time seems linear as well, but didn't converge as well in 100 iterations.

  ## Part5. Hawkes Process in Finance
  
  - The fit of Hawkes Model to the limit order book
  
  ![image](https://user-images.githubusercontent.com/110284601/184845407-09028fa9-be43-4ecd-baea-207cc0fa54cc.png)  


  - Systematic analysis.
  
  To test for goodness of fit, we used a KS test for a uniformly distributed variable on the transfuced times. Higher p-values indicate good fit, and we used a threshold of 0.9. The test is passed 7% of the time, which indicates rather poor goodness of fit.
  
  ![image](https://user-images.githubusercontent.com/110284601/184845528-8f4aa1f3-c415-423e-9756-d0f5b6347001.png)

  As expected, the p-value of the KS test increases with the numbr of exponential kernels on longer samples, which indicates a better fit. The highest p-value remains small (around 0.13), which could be explained by the fact that we averaged on all the value of number of linear pieces in the baseline.
  
  ![image](https://user-images.githubusercontent.com/110284601/184845588-9ed5b865-52d4-4a53-b88f-0cde98609855.png)
  
  Using only the highest value of number of linear pieces in the baseline allows to reach better goodness of fit as expected.

  ![image](https://user-images.githubusercontent.com/110284601/184845664-34dc9c91-a24b-4e45-ae3d-4c34c3dec2ca.png)
  ![image](https://user-images.githubusercontent.com/110284601/184845685-53e0d6d2-8936-4ba3-b05f-e1825f03f4d8.png)
  ![image](https://user-images.githubusercontent.com/110284601/184845704-1d306655-6b08-4b00-b595-4cca5014c6bf.png)
  
  Branching ratio increases with the number of kernels (which is not surprising since adding kernels adds terms to the sum in the definition of the branching ratio), and with the sample length (which probably means that when the sample length gets too high, the baseline intensity has to be low enough to accomodate for the least active parts of the day, and the remaining activity has to be added with endogeneity). It decreases with the number of pieces in the baselines, which further coroborates this last point, as more pieces means that the model can acomodate with the more and less active parts of the day with the baseline.

  ![image](https://user-images.githubusercontent.com/110284601/184845752-4b37d2ed-ff39-44fc-a81f-7e9628be9c37.png)
  ![image](https://user-images.githubusercontent.com/110284601/184845785-a7dcc3ef-c1b6-4d3a-8101-f4fd9991d793.png)
  
  The number of kernels chosen with the AIC does not seem to depend on the number of pieces in the baseline. However, it clearly increases with the sample length, which further proves the firts point of this section that longer sample length require more kernels.

  ## Part6. Poisson Process and Limit Order Book - Perfect Market Making
  
  - Sanity check
  
  ![image](https://user-images.githubusercontent.com/110284601/184846439-29dcc6a0-b5f9-4887-b9bc-db20f1b2dbab.png)
  
  The above plot and prints allow us to check that the last transition worked as expected. Changing the index of the events in the history h allowed us to chech other individual events at will, and we did not notice any irregularity.
  
  We change the arbitrary floats representing time to a datetime format (assuming that the floats represent a number of seconds, even though it does not necessarly), in order to use sampling methods in later questions.
  
  ![image](https://user-images.githubusercontent.com/110284601/184846591-b4851a8e-831e-4ffd-8f2f-d4eeb923fa8a.png)
  
  We excpect the intensity of the time of events to be around  2𝜇+2𝐾𝜆+10𝐾𝜃=55  (because the initial values of the volumes are at 5, so we expect  5𝜃  to be close to the average intensity of the times of arrival for cancellation order on a given position of the window). Therefore, we excpect to have ~30 000 events in our simulation, which is the case. The relative number of events in each category are also distributed as expected (the event of the same type (market order/limit order/cancellation) have similar numbers of occurence regardless of the side of the lob they were related to; we excpected to have 6 times more limit orders than market orders based on the values of  𝜇  and  𝐾𝜆 , which is verified)


  - Simulation of limit order book

  ![image](https://user-images.githubusercontent.com/110284601/184846654-09e7d1b2-1e46-4006-80bb-77511d4bbaeb.png)
  
  The average shape of the LOB is as expected, with a dip in volumes close to the spread.The peaks in the LOB right after and before the spread also make sense: neglecting the market orders, the initial value of X imposes that the volumes further away stay around 5, and the shape in between depends on the relative intensities of limit orders and cancellations. Here, we have significantly more limit orders, hence the peaks.
  
  ![image](https://user-images.githubusercontent.com/110284601/184846708-b9cd45f1-2491-451f-9a05-46599e213ecc.png)
  
  As expected, the variation of the med price seems centered (the model is symetric between asks and bids), and is mostly confined to small values (smaller than 0.5), which is not surprising, as a large change in mid price requires a change twice as large in the spread, and since the spread mostly varies between 1 and 2, it can't vary too much either.

  ![image](https://user-images.githubusercontent.com/110284601/184846761-9782ab63-932a-4907-9bda-f97a208b932c.png)
  
  As expected, for shorts sampling periods, the variation of the mid price spikes at 0, and the larger the sampling period, the wider the distribution of mid variation.
  
  ![image](https://user-images.githubusercontent.com/110284601/184846823-770098b1-0ad0-413d-83d8-905bd8bbaf55.png)
  
  The model does not show memory in the mid price variation, which is to be expected, as the events are independant from each other.

  ![image](https://user-images.githubusercontent.com/110284601/184846877-e17f8f5e-988f-4fd3-946b-5aee0bfccd07.png)
  
  As expected from the distributions plotted previously, the variance increases with the sampling period. Early on, the variance increases faster, but the rate of progression stabilizes once a sampling period of around 10secs is reached, probably because we can add a lot of variance by removing the peak at 0 in the small sampling periods.


  
  

