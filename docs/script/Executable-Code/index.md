# Executable code

Executable code is code that is executed by the game during runtime to alter the gameplay.

## Execution conditions

Code will execute in one of three conditions:

- It is declared an [action](/script/Objects/Actions), and the user performs that action.

- It is declared inside a [function](/script/Objects/Functions), and other code calls that function.

- It is run from a [debug command](/gameplay/debug-command).


## Parsing

Each line of code is parsed and run one by one. Executing multiple actions in one line is not supported, each action must be separated by a line break.



### 