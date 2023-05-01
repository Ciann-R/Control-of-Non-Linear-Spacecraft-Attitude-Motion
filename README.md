
# Control Of Non Linear Spacecraft Attitude Motion.

## Simulating a general spacecraft motion where a control torque u is being applied.

The control torque "u" in each case provides for a globally asymptotically stabilizing non-linear control feedback law which is derived via Lyapunov's direct method; "u" of course can be modified depending on wheter one is interested soley on the attitude descriptions (i.e a spacecraft tracking problem) or the rotational rate descriptions (i.e a tumbling/rotating spacecraft problem). Nevertheless, a general construction of "u" is formulated via a linear combination of the elemental position and velocity based Lyapunov functions in the MRP attitude description set. Lyapunov's direct method is a rigorous scheme of proving stability of non-linear systems by means of analysing the behaviour of a scalar energy-like Lyapunov function about a reference/target state on its domain. To elaborate briefly, if a Lyapunov function V(x) exists for some dynamical system dx/dt = f(x), it is implied that the system is infact stable about the origin/reference. However, the  negation of this statement does not imply instability; instead, if one cannot form a suffiecient Lyapunov function V(x) for the dynamical system, the theroem holds inconclusive. Therefore, the theorem can only be used to explicitly make claims about a systems stability or instability. In any manner, The conditions upon which V(x) is considered a Lyapunov function are as follows:

 **1)** V(x) is a positive definite function about the reference state x_r.

 **2)** V(x) has continuous partial derivatives.

 **3)** dV(x)/dt is negative semidefinite.

The Lyapunov function is radially unbounded (i.e: V(x) tends to infinity as ‖x‖ tends to infinity) thus infering global stability. Moreover, V(x) is asymptotically stabilizing if the following conditions are true, firstly, the system is stable about x_r(t) and secondly, dV(x)/dt is negative definite about x_r(t).
Several variations of the control torque "u" are implemented (as outlined below), for a simple model of some arbitrary spacecraft with a predefined inertia matrix [I] and typically with some initial positions and velocities relative to the inertial frame of reference. The attitude and angular rate descriptions of the spacecraft relative to the inertial frame of reference, along with the attitude and angular error rate descriptions are plotted and their norms subsequently computed. The attitude and angular error rate descriptions of the spacecraft describe the discrepency between its inertial descriptions of the craft relative to the reference attitude and angular rate descriptions. The reference descriptions are the desired target values, which one aims for the spacecraft to achieve over some arbitrary time via the implementation of the control torque "u". 

The regulator and tracking cases are developed for each control torque implemented. Futher details are expounded in the notebook.


#### **Case 0:** Implementing the general globally stabilizing control solution in the absence of external torques (i.e: L = 0).

#### **Case 1:** Implementing the simplified general globally stabilizing control solution.

#### **Case 2:** Implementing the simplified general globally stabilizing control solution with integral control feedback. 

#### **Case 3:** Optimal control feedback. Implementing the simplified general globally stabilizing saturated control solution.

#### **Case 4:** Linear closed loop control.

