# Macro Examples

## Encrypt String
```lua
print(ENC_STR("Hello World"))
```

## Hide Global
```lua
HIDE_GLOBAL(print)("Hello World")
```

## Junk Code
```lua
for i=1,10 do
    JUNK_CODE()
    print("Hello World")
end;
```

## Compiler Expression
```lua
CMP_EXPR("MaxAmount", 10)

local Money = 11;
if Money > MaxAmount then
    print(string.format("You have gone $%d over your limit", Money - MaxAmount))
end;
```

## Protected FireServer
```lua
local Event = game.ReplicatedStorage.GunFired
local Gun = require(game.ReplicatedStorage.Modules.Weapon)

Gun.Fired.Event:Connect(function(position) 
    JSEC_FireServer(Event, position)
end)
```

## Protect Table
```lua
local module = { firerate = 2, reloadspeed = 1.5, maxammo = 10, currentammo = 10 }
return PROTECT_TABLE(module)
```