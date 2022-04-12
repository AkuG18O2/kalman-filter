# Kalman Filters
MATLAB/Simulink implementation of Kalman filters and its non-linear variants

## Linear Kalman Filter
* Kalman Filter is an optimal state observer
* Also called Linear Quadratic Estimation (LQE)
* Works for linear systems
* Takes into account statistical noise
* Combines estimated and measured readings from different sources using joint probability distribution to estimate an optimal reading

***Process noise (wk):*** Noise due to inexact nature of modelled physical equations, such as deviations due to air pressure. Needs to be tuned.
***Measurement noise (vk):*** Noise characteristic to the sensor's working. Needs to be obtained from sensor calibration.

* Both wk and vk can be assumed to be mutually uncorrelated white Gaussian noise processes.

* The state-space equations of the system are:

![image](https://user-images.githubusercontent.com/32334432/162919664-ca5e52a0-060f-470d-9d02-ece26e9c98f2.png)

* In control theory, a **state observer** or state estimator is a system that provides an estimate of the internal state of a given real system, from measurements of the input and output of the real system.

![image](https://user-images.githubusercontent.com/32334432/162919731-54f6ddf3-9119-4982-8bdd-3983a43b1f7b.png)

![image](https://user-images.githubusercontent.com/32334432/162919737-dd33a50d-8d07-4d86-b900-9796b4f7a092.png)

* In essence, Kalman filter has two steps: **Predict** and **Update**

![image](https://user-images.githubusercontent.com/32334432/162920018-0a6eb372-89ca-4e07-b500-f9ad68cc65ee.png)

![image](https://user-images.githubusercontent.com/32334432/162920033-cc75ea80-73bd-4816-9921-d0ea8835d4d6.png)

![image](https://user-images.githubusercontent.com/32334432/162920045-adbb0768-0b65-4131-84e8-fa9d6ffdeec8.png)

![image](https://user-images.githubusercontent.com/32334432/162920052-d96b19a3-c5b5-4560-a2cf-1201490eed29.png)

## Non-linear systems

![image](https://user-images.githubusercontent.com/32334432/162920192-c0b24206-25a0-435b-92cf-27cc12027bf4.png)

![image](https://user-images.githubusercontent.com/32334432/162920208-4a64f582-c40b-448c-9c8f-aa2914e11c33.png)
![image](https://user-images.githubusercontent.com/32334432/162920225-6ac284a0-dba5-4a9c-9e2f-2c6522c6a6c7.png)

### Sigma points

![image](https://user-images.githubusercontent.com/32334432/162920300-e2c3a74d-3d29-4728-bc11-ad8681d78bad.png)
![image](https://user-images.githubusercontent.com/32334432/162920317-26a879f5-afdf-43f9-b7ba-d0eb0f958f52.png)

## Modelling

**Linear model**
![image](https://user-images.githubusercontent.com/32334432/162920911-08422b89-5b0f-4af1-994b-9fc9fed01fde.png)

**Non-linear model**
![image](https://user-images.githubusercontent.com/32334432/162920954-5eeab3c6-2ec5-4363-ae65-40eeac287291.png)

**Kalman filter**
![image](https://user-images.githubusercontent.com/32334432/162921021-1b28f973-13c9-472b-a0ed-511ad90cb3ee.png)

**Extended kalman filter**
![image](https://user-images.githubusercontent.com/32334432/162921037-d4b52293-d8fe-4142-8493-331aedbc55cd.png)

**Unscented kalman filter**
![image](https://user-images.githubusercontent.com/32334432/162921051-0f81a068-c364-42e7-b3e3-f948d6d6ba25.png)

## Demo

![image](https://user-images.githubusercontent.com/32334432/162921161-9e39c86e-64a9-4789-9d10-c5bbbaceb32a.png)

## Follow up
* Tuning of kalman filter parameters and initial state assumptions
* Normalized error visualization
* Implementation of particle filter for non-gaussian system
* Model a real system and compare results with actual hardware testing

## Applications in electronics
* Battery pack state of charge estimation using ESC cell model
* Sensorless motor drive control and state estimation
* Automotive navigation systems and sensor fusion
* Image processing and noise removal

## References
* https://in.mathworks.com/help/control/ug/extended-and-unscented-kalman-filter-algorithms-for-online-state-estimation.html
* https://groups.seas.harvard.edu/courses/cs281/papers/unscented.pdf
* https://in.mathworks.com/help/control/ug/nonlinear-state-estimation-using-unscented-kalman-filter.html
* https://academic.csuohio.edu/simond/pubs/ESDNonlinear.pdf
* https://ieeexplore.ieee.org/document/7530343
* https://ieeexplore.ieee.org/document/7734116

