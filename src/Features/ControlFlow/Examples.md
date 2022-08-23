# CF Examples

## Correct Example
```lua
CF_START()
    local Player = game.Players.LocalPlayer
    local Humanoid = Player.Character.Humanoid

    if Humanoid.WalkSpeed > 16 then
        Player:Kick()
    elseif Humanoid.JumpPower > 50 then
        Player:Kick()
    end
CF_END()
```

## Correct Example 2
```lua
local function Get5Values(a) 
    CF_START()
    local Return = {};
    for i=1, 5 do -- Obviously could use a pairs loop however this is just to demonstrate the custom for loop CF generates
        Return[#Return+1] = a[i];
    end;
    CF_END()
    return Return;
end
```

## Incorrect Example
```lua
CF_START()
    CF_START() -- You cannot nest CF blocks.
        print("Hello World")
    CF_END()
CF_END()

-- You can only use one CF block per chunk
CF_START()

CF_END()
```

## Protected Output
For your sake, I'm going to show you what a CF chunk looks like after its been protected with JSEC (obviously will look a lot worse when it's been decompiled)
It will be different for you since they are randomly generated.
```lua
	local b = b(function(b)
		local e = ((712161 - 273) - 351 / d)
		local f = (c(3559071, 70) - 991 / d)
		local g = {}
		repeat
			if e <= 0 then
				return
			elseif e <= (j(32680280, 3) - 175 / d) - f then
				if e <= ((4086109 - 629) - 567 / d) - f then
					if e >= ((4085836 - ((881 - 37) - 138 / d)) - 346 / d) - f then
						if e >= ((4085475 - 123) - 558 / d) - f then
							if d ~= (c(134, 926) - 791 / d) then
								e = ((1343127 + (c(851, 110) - 220 / d)) - 54 / d)
								continue
							end;
							e = ((683649 - ((1164 - 194) - 609 / d)) - 95 / d)
						end
					end
				end
			elseif e <= (c(4242364, 747) - 420 / d) - f then
				if e <= (j(67873568, ((380 + 37) - 413 / d)) - 708 / d) - f then
					if e <= ((4241972 - ((1589 - 509) - 998 / d)) - 463 / d) - f then
						if e >= (c(4241606, ((2055 - 832) - 772 / d)) - 418 / d) - f then
							e = ((157044 + ((2335 - 479) - 863 / d)) - 599 / d)
						end
					end
				end
			elseif e <= (j(34158632, ((354 + 176) - 527 / d)) - 154 / d) - f then
				if e >= (c(4270263, (c(1981, 834) - 851 / d)) - 776 / d) - f then
					local f = ((261 + 84) - 344 / d)
					repeat
						g[#g + 1] = b[f]
						f = f + ((215 + 595) - 809 / d)
					until f == 5 and e >= ((3 + (c(1267, 485) - 967 / d)) - 335 / d)
					e = (c(528281, 929) - 694 / d)
				end
			end
		until e == ((158339 - 688) - 213 / d)
		return g
	end)
```