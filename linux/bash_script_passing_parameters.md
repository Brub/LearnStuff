# Bash script - passing parameters
You can pass parameters to a bash script. This is used when you want your script to perform in a different way, depending on the values of the input parameters (also called arguments).

In fact, it's pretty simple. You can access an argument inside a script using the variables $1, $2, $3, and so on. The variable $1 refers to the first argument, $2 to the second argument, and $3 to the third argument.

example bash script:

```
#!/bin/bash

ARG1=$1

if [ $ARG1 == 'forward' ]; then
    rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: -0.1
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0"

elif [ $ARG1 == 'rotate' ]; then
    rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.2"

elif [ $ARG1 == 'stop' ]; then
    rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0"
fi
```