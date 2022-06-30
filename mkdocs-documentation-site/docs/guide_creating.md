# Creating a quaternion
There are several ways you can create a quaternion. The simplest one being `QuaternionModule.new()`.
Below is an example of how to create a quaternion:

```lua
-- Get the ReplicatedStorage service
local sRepStorage = game:GetService("ReplicatedStorage");

-- Require the quaternion module
local qtModule = require(sRepStorage.QuaternionModule);

-- Create a new identity Quaternion
local quaternion = qtModule.new();

-- WXYZ arguments are also supported
quaternion = qtModule.new(1,0,0,0);
```

!!! note tip "Tip"

    QuaternionModule.new() uses the WXYZ parameter order, so make
	sure the W argument always goes first.

## Converting to a quaternion

You can also convert Euler angles (both degrees and radians) as well as CFrame-s into quaternions,
and vice versa. Below is a list of ways you can do that.

!!! note tip "Tip"

    Keep in mind that converting from Euler angles to Quaternion uses the XYZ order.

### From Euler angles in degrees

```lua
-- For converting XYZ, use qtModule.fromEulerDegA()
local quaternionA = qtModule.fromEulerDegA(45, 90, 0);

-- For converting a Vector3, use qtModule.fromEulerDegB()
local quaternionB = qtModule.fromEulerDegB(Vector3.new(45, 90, 0));
```

### From Euler angles in radians

```lua
-- For converting XYZ, use qtModule.fromEulerRadA()
local quaternionA = qtModule.fromEulerRadA(0.785398, 1.5708, 0);

-- For converting a Vector3, use qtModule.fromEulerRadB()
local quaternionB = qtModule.fromEulerRadB(Vector3.new(0.785398, 1.5708, 0));
```

### From CFrame

```lua
local quaternion = qtModule.fromCFrame(CFrame.new());
```

## Converting from a quaternion

You can also convert a quaternion back into a CFrame or an Euler angle.
Below is a list of ways you can do that.

!!! note tip "Tip"

    Keep in mind that converting from Quaternion to Euler angles uses the XYZ order.

### To Euler angles in degrees

```lua
local quaternion       = qtModule.new();
local vector3InDegrees = quaternion:ToEulerDegrees();
```

### To Euler angles in radians

```lua
local quaternion       = qtModule.new();
local vector3InRadians = quaternion:ToEulerRadians();
```

### To CFrame

```lua
local quaternion = qtModule.new();
local cframe     = quaternion:ToCFrame();
local cframeWPos = quaternion:ToCFrame(Vector3.new(0,10,0)); -- With position
```

### To string

```lua
local quaternion = qtModule.new();
local str        = quaternion:ToString(); -- Result: "1,0,0,0"
```

## Notice

Creating a quaternion returns a table containing the WXYZ fields, as well
as functions related to quaternions. For more info, please see [this page](api_quaternion.md).
To begin working with quaternions, and performing mathematical operations, see [this page](guide_math.md).