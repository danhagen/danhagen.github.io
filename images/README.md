# README.md for Figures Created 2020/04/22 at 17:30.09

## Notes

Rerunning to show _actual_ trajectory in histograms. Previous versions forced the bins to be between the maximum and minimum joint angles. Stiffness was not forced to be anywhere, so this is good news for the stiffness plots.

## Parameters

 ```py
 params = {
	'Extra Steps' : 3,
	'Step Duration' : 2.0,
	'angleRange' : [2.356194490192345, 3.9269908169872414],
	'frequency' : 1,
	'stiffnessRange' : [20, 100],
	'numberOfSteps' : 100,
	'delay' : 0.3
}
```

## Figures

#### states_01-01.png

<p align="center">
	<img width="500" src="states_01-01.png">
</p>

#### states_01-02.png

<p align="center">
	<img width="500" src="states_01-02.png">
</p>

#### states_01-03.png

<p align="center">
	<img width="500" src="states_01-03.png">
</p>

#### states_01-04.png

<p align="center">
	<img width="500" src="states_01-04.png">
</p>

#### states_01-05.png

<p align="center">
	<img width="500" src="states_01-05.png">
</p>

#### all_states_and_inputs_01.png

<p align="center">
	<img width="500" src="all_states_and_inputs_01.png">
</p>

### NOTE
The tendon tension and motor torques are *highly* correlated. The Pearson coefficients are ~0.999959 for both motor-tendon complexes. This would imply that it would be equivalent to replace the **difficult to measure** tendon tensions in our predictor algorithms with the readily available motor torques. In biology, we do have efference copies, but these do not directly correlate to tendon tension as they have to contend with nonlinear force-length, force-velocity relationships. Additionally, this is for a system that has not contact with the world. If the pendulum were to experience a sudden impact, the tendon tensions would change instantly, but the motor torques would deviate. But if the controller was predictive or proportional, then it would be likely that the motor torques would eventually become correlated again.
