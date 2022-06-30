# QuaternionOperators

This module is used by the quaternion metatable to allow for use of
mathematical operators on quaternions. You do not need to `require()`
this module in order to perform mathematical operations on quaternions.

!!! note tip

    Keep in mind that unlike in [Quaternion](api_quaternion.md)s,
	using these functions **will not** directly affect the quaternions
	that have been passed as arguments.
	All functions here return a separate quaternion copy.

## Functions

??? note note "NegateQ(qt : Quaternion) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Returns a negated copy of a given quaternion.

??? note note "AddQQ(qt1 : Quaternion, qt2 : Quaternion) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Adds two quaternions.

??? note note "SubtractQQ(qt1 : Quaternion, qt2 : Quaternion) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Subtracts two quaternions.

??? note note "MultiplyQQ(qt1 : Quaternion, qt2 : Quaternion) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Multiplies two quaternions.

??? note note "MultiplyQN(qt : Quaternion, num : number) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Multiplies a quaternion with a number.

??? note note "DivideQQ(qt1 : Quaternion, qt2 : Quaternion) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Divides two quaternions.

??? note note "DivideQN(qt : Quaternion, num : number) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Divides a quaternion by a number. Please avoid dividing by zero.