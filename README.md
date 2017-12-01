# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

# Reflection
## Effect of P - Component of PID Controller
The P in PID stands for "proportial", which means, that the control deviation (error) is multiplied by a (negative) factor and fed back as an input.
This is very easy to calculate, but also causes a bad behaviour. The car is oscillating around the target.

## Effect of I - Component of PID Controller
The I in PID stands for "integral", which means, that the control deviation (error) is being integrated/added over time, multiplied by a factor and fed back as an input.
This part of the controller takes care of offsets and forces the system to the target value.

## Effect of D - Component of PID Controller
The D in PID stands for "differential", which means, that the change of control deviation (error) is taken into account. This is simply done by the relation between the last error and the current error.
This part of the controller brings smoothness as oscillations are reduced.

## How to choose PID parameters
I set the values manually, as I was not able to get working parameters using the twiddle algorithm.
I started with the Controller for steering angle, and chose P and D, so that I was satisfied with the car oscillation. The I component was the chosen small in order to react to trajectory problems when going close to the border of the track.
The PID for acceleration was chosen in the same way. Using my PID parameters, I was able to set the target speed to 70mphs.

