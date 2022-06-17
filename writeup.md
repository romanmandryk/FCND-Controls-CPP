The QuadControl.cpp is now implemented and params tuned to satisfy all 5 criteria (without optional subtasks in scenario 5- after generating trajectory with velocity I was unable to tune the quad to pass criterai).

Implemented body rate control in C++.
----
BodyRateControl method

Implement roll pitch control in C++.
--
RollPitchControl method 

Implement altitude controller in C++.
--
AltitudeControl method
For scenario 1-3 (before adding integrator) see commit https://github.com/udacity/FCND-Controls-CPP/commit/5a026ede878d04834c56c34f5e866497712a3ac2
For final implementation with integrator see latest commit on master branch

Implement lateral position control in C++.
--
LateralPositionControl method

Implement yaw control in C++.
--
YawControl method

Implement calculating the motor commands given commanded thrust and moments in C++.
--
First implementation (in previous commits) had a wrong assumption about L being proper length. 
After reading https://knowledge.udacity.com/questions/128899 I changed implementation and fortunately had to re-tune 
only kpPQR gain as only inner-most controller was affected (BodyRates)