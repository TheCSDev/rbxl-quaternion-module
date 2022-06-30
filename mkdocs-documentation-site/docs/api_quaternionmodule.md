# QuaternionModule

The main quaternion module. This module is used for creation of quaternions.

!!! note warning "Note"

	Please keep in mind that whenever you see the `Quaternion` type mentioned,
	it is actually referring to a `table`. For example, `ToString(self : Quaternion)`
	is actually `ToString(self : table)` because quaternions are just regular tables.<br/>
	<br/>
	In other words, do not use `type(quaternion) == 'Quaternion'`, instead use `type(quaternion) == 'table'`.

## Constructors

??? note note "new(w : number?, x : number?, y : number?, z : number?) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Creates a new quaternion. The arguments are optional.

??? note note "fromCFrame(arg0 : CFrame) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Creates a new quaternion from a CFrame.

??? note note "fromEulerRadA(roll : number, pitch : number, yaw : number) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Creates a new quaternion from XYZ Euler angles in radians.

??? note note "fromEulerRadB(arg0 : Vector3) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Creates a new quaternion from Vector3 Euler angles in radians.

??? note note "fromEulerDegA(roll : number, pitch : number, yaw : number) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Creates a new quaternion from XYZ Euler angles in degrees.

??? note note "fromEulerDegB(arg0 : Vector3) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Creates a new quaternion from Vector3 Euler angles in degrees.

## Functions

??? note note "Lerp(qt1 : Quaternion, qt2 : Quaternion, amount : number) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Linearly interpolates between two given quaternions.
	Returns a new quaternion, without affecting any given quaternions.

??? note note "Slerp(qt1 : Quaternion, qt2 : Quaternion, amount : number) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Interpolates between two given quaternions, using spherical linear interpolation.
	Returns a new quaternion, without affecting any given quaternions.