# Quaternion Module

The [QuaternionModule](api_quaternionmodule.md) script allows you to work with quaternions more easily,
without needing to create your own module for it. This documentation contains
information on how to use the module script to create your own quaternions and
work with them, as well as information on all available functions you can use.

## Getting started

To get started, you will need to `require()` the module script. This documentation
assumes you have placed the [QuaternionModule](api_quaternionmodule.md) into the
[ReplicatedStorage](https://developer.roblox.com/en-us/api-reference/class/ReplicatedStorage).

```lua
-- Get the ReplicatedStorage service
local sRepStorage = game:GetService("ReplicatedStorage");

-- Require the quaternion module
local qtModule = require(sRepStorage.QuaternionModule);
```

Once you have `require()`d the module, you can then use it to create quaternions.
To get started, see [this page](guide_creating.md).