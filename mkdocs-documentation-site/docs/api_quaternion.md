A table that represents a quaternion.

!!! note warning "Note"

	Please keep in mind that whenever you see the `Quaternion` type mentioned,
	it is actually referring to a `table`. For example, `ToString(self : Quaternion)`
	is actually `ToString(self : table)` because quaternions are just regular tables.<br/>
	<br/>
	In other words, do not use `type(quaternion) == 'Quaternion'`, instead use `type(quaternion) == 'table'`.

## Fields

??? note note "W : number"
	**Type:** number<br/>
	**Default value:** 1<br/>
	<br/>
	The W value of the quaternion

??? note note "X : number"
	**Type:** number<br/>
	**Default value:** 0<br/>
	<br/>
	The X value of the quaternion

??? note note "Y : number"
	**Type:** number<br/>
	**Default value:** 0<br/>
	<br/>
	The Y value of the quaternion

??? note note "Z : number"
	**Type:** number<br/>
	**Default value:** 0<br/>
	<br/>
	The Z value of the quaternion

## Functions

### General functions

??? note note "new(w : number?, x : number?, y : number?, z : number?) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Creates a new quaternion. This isn't the intended way of creating quaternions,
	but it can be done this way as well. This constructor was included here in
	quaternions as well for technical reasons.

??? note note "Clone(self : Quaternion) : Quaternion"
	**Returns:** table (Quaternion)<br/>
	<br/>
	Clones the given quaternion and returns the copy.

??? note note "ToString(self : Quaternion) : string"
	**Returns:** string<br/>
	<br/>
	Returns an WXYZ string representation of the quaternion.<br/>
	Example: 1,0,0,0

### Conversion functions

??? note note "ToCFrame(self : Quaternion, position : Vector3?) : CFrame"
	**Returns:** CFrame<br/>
	<br/>
	Converts the quaternion to a CFrame, and then returns the CFrame.<br/>
	The position argument is optional. It's default value is Vector3.new().

??? note note "ToEulerRadians(self : Quaternion) : Vector3"
	**Returns:** Vector3<br/>
	<br/>
	Converts the quaternion to an Euler angle Vector3, in radians.

??? note note "ToEulerDegrees(self : Quaternion) : Vector3"
	**Returns:** Vector3<br/>
	<br/>
	Converts the quaternion to an Euler angle Vector3, in degrees.

### Math functions (returns number)

??? note note "Length(self : Quaternion) : number"
	**Returns:** number<br/>
	<br/>
	Calculates the length of the Quaternion.

??? note note "LengthSquared(self : Quaternion) : number"
	**Returns:** number<br/>
	<br/>
	Calculates the length squared of the Quaternion.

??? note note "Dot(self : Quaternion, quaternionB : Quaternion) : number"
	**Returns:** number<br/>
	<br/>
	Calculates the dot product of this and a given Quaternion.

### Math functions (returns self)

!!! note warning "Warning"

    Keep in mind that using these functions directly affect the quaternion.
	If you wish to apply a change to a separate quaternion, please
	use the `Clone()` function.<br/>
	For exapmle: `local qtNormalized = quaternion:Clone():Normalize();`.

??? note note "Normalize(self : Quaternion) : Quaternion"
	**Returns:** self<br/>
	<br/>
	Divides each component of the Quaternion by the length of the Quaternion.

??? note note "Conjugate(self : Quaternion) : Quaternion"
	**Returns:** self<br/>
	<br/>
	Conjugates the quaternion.

??? note note "Inverse(self : Quaternion) : Quaternion"
	**Returns:** self<br/>
	<br/>
	Inverses the quaternion.

??? note note "Concatenate(self : Quaternion, quaternionB : Quaternion) : Quaternion"
	**Returns:** self<br/>
	<br/>
	Concatenates the quaternion.

??? note note "Lerp(self : Quaternion, quaternionB : Quaternion, amount : number) : Quaternion"
	**Returns:** self<br/>
	<br/>
	Linearly interpolates between this and a given quaternion.

??? note note "Slerp(self : Quaternion, quaternionB : Quaternion, amount : number) : Quaternion"
	**Returns:** self<br/>
	<br/>
	Interpolates between this and a given quaternion, using spherical linear interpolation.