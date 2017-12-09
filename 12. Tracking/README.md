# Filtering distribution
* given observations up to time t, predict current state x_t
* P(x_t|e_1:t)
* The evaluation of Bel(x_t) = P(x_t|e_1:t) is recursive
	* Bel(x_t) = P(e_1:t|x_t) * sum_{x_{t-1}} P(x_t|x_t-1) Bel(x_{t-1})

# Prediction distribution
* given observations up to time t, prediction future state t+k
* P(x_{t+k}|e_1:t)

# Smoothing distribution
* given observations up to time t, prediction past state k
* P(x_k|e_1:t) for k < t

# Best sequence 
* find the best states sequence x_1:t
* argmax P(x_1:t|e_1:t)

# Kalman filter
* Kalman filter involves a few steps:
	* deterministic drift from posteriror from last step
	* stochastic diffusion
	* incorporate data
![Kalman filter](https://github.com/junweima/computer_vision_summaries/blob/master/12.%20Tracking/images/kalman_filter.jpg)


