# Quaternion Module

The [QuaternionModule](https://thecsdev.github.io/rbxl-quaternion-module/api_quaternionmodule/) script allows you to work with quaternions more easily,
without needing to create your own module for it. This documentation contains
information on how to use the module script to create your own quaternions and
work with them, as well as information on all available functions you can use.

## Getting started

### Installing the Quaternion module
1. Open the `QuaternionModule.rbxl` file in [Roblox Studio](https://www.roblox.com/create)
2. In the Explorer, locate `ReplicatedStorage`, in there you will find the `QuaternionModule` script
3. Copy the module script and paste it into your own project (into `ReplicatedStorage`)
4. Make sure any children of the module script were properly copied as well
5. You are ready to start working with the Quaternion module

### Working with the Quaternion module

To get started, you will need to `require()` the module script. The documentation
assumes you have placed the [QuaternionModule](https://thecsdev.github.io/rbxl-quaternion-module/api_quaternionmodule/) into the
[ReplicatedStorage](https://developer.roblox.com/en-us/api-reference/class/ReplicatedStorage).

```lua
-- Get the ReplicatedStorage service
local sRepStorage = game:GetService("ReplicatedStorage");

-- Require the quaternion module
local qtModule = require(sRepStorage.QuaternionModule);
```

Once you have `require()`d the module, you can then use it to create quaternions.
To get started, see [this page](https://thecsdev.github.io/rbxl-quaternion-module/guide_creating/).
