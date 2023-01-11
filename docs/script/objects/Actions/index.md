# Actions

Actions are [functions](../Functions) that are called when the user enters text matching their name.

An action is the only object to be able to have multiple identifyers.

## Declaration

To declare an action, use `action` followed by its identifyers, separated by commas, like so:

```
action light, ignite:
```

<p style="font-size:7px;">(I have no idea if it works with multiple words so just try to keep it as one word)</p>

Any text after the declaration tag will be considered [executable code](/script/Executable-Code) and run when the user performs the action, 
unless a declaration tag of another object is detected.

Indentation does not matter, but keeping good indentation is recommended.