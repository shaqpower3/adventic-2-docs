# Global variables

Global variables are variables on the bottom of the [variable stack](/engine/varstack), they can be accessed from any piece of executed code.

## Declaration

To declare a global variable, use `keep track of`, `track` or `globvar`, like so:

```
globvar name
```

### Value assignment

To assign a default value to the variable, use any of the following:

- `name is 5`

- `it is 5`

- `it's 5`

- `its 5`

- `=5`

Like so:

```
globvar name:
    =5
```