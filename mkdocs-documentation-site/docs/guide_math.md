# Math operations

In terms of operators, quaternions support addition, subtraction, multiplication
with numbers and quaternions, division with numbers and quaternions, as well
as the unary minus operator (-value). 
 
Quaternions also offer other math related functions such as `Length()`, `LengthSquared()`,
`Dot()` and so on. More info can be found [here](api_quaternion.md).

## Operators

### Unary minus

Returns a new negated quaternion of the given quaternion.
```lua
local quaternion = qtModule.new();
local qtNegated  = -quaternion;
```

### Addition

Returns a new quaternion with the two given quaternions added together.
```lua
local quaternionA = qtModule.new();
local quaternionB = qtModule.new();
local qtSum       = quaternionA + quaternionB;
```

### Subtraction

Returns a new quaternion with the two given quaternions subtracted.
```lua
local quaternionA  = qtModule.new();
local quaternionB  = qtModule.new();
local qtDifference = quaternionA - quaternionB;
```

### Multiplication

Returns a new quaternion with the two given quaternions multiplied.
```lua
local quaternionA = qtModule.new();
local quaternionB = qtModule.new();
local qtProductA  = quaternionA * quaternionB;
local qtProductB  = quaternionA * 2; -- Numbers are also supported
```

### Division

Returns a new quaternion with the two given quaternions multiplied.
```lua
local quaternionA = qtModule.new();
local quaternionB = qtModule.new();
local qtQuotientA = quaternionA / quaternionB;
local qtQuotientB = quaternionA / 2; -- Numbers are also supported
-- Try to avoid dividing by zero. Weird things can happen.
```

## Functions

Quaternions also feature some math related functions to help you
work with them. For a full list of all functions, please see
[this page](api_quaternion.md).

!!! note warning "Warning"

    Keep in mind that using those functions directly affect the quaternion.
	If you wish to apply a change to a separate quaternion, please
	use the `Clone()` function.<br/>
	For exapmle: `local qtNormalized = quaternion:Clone():Normalize();`.

Below are some of the functions

```lua
-- Create a new quaternion
local qt = qtModule.new();

-- Functions that return numbers
local qtLength        = qt:Length();        -- less performant
local qtLengthSquared = qt:LengthSquared(); -- more performant

-- Functions that return quaternions
local qtNormalized   = qt:Clone():Normalize();
local qtConjugated   = qt:Clone():Conjugate();
local qtInversed     = qt:Clone():Inverse();
local qtConcatenated = qt:Clone():Concatenate(qtModule.new());
local qtLerped       = qt:Clone():Lerp(anotherQuaternion, 0.5);
local qtSlerped      = qt:Clone():Slerp(anotherQuaternion, 0.5);
```