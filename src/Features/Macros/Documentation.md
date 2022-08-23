# Macro Documentation

## Encrypt String
Encrypts a string when protected, decrypts on runtime.
```lua
<string> ENC_STR(<string>)
```

## Hide Global
Encrypts the global name, decrypts on runtime and grabs from the environment.
```lua
<global> HIDE_GLOBAL(<global>)
```

## Junk Code
Inserts some junk code at the location of where you called the macro.
```lua
JUNK_CODE()
```

## Compiler Expression
When JSEC compiles your script all instances of `name` will be replaced with `value`
```lua
CMP_EXPR(<string name>, <string value>)
```

## Protected FireServer
A secure varient of .FireServer, will attempt to anonymise the calling script.
```lua
JSEC_FireServer(<RemoteEvent event>, ...<arguments>)
```

## Protect Table
Will protect the inputted table against unknown environments calling __index.
```lua
<table> PROTECT_TABLE(<table>)
```