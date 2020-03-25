# Geometric-PhaseOPENQASM 2.0;
include "qelib1.inc";

qreg q[5];
creg c[5];

h q[0];
u1(pi/2) q[1];
cx q[0],q[1];
u3(pi/2,pi/2,pi/2) q[1];
cx q[0],q[1];
h q[0];
u3(pi/2,pi/2,pi/2) q[1];
measure q[0] -> c[0];
