# GAME PROGRAMMING - EX - 4

## EXP - 4 Attach Rifle with character mesh and implementation bullet spawn from Rifle

## Name : PRAGATHI KUMAR
## Reg no : 212224230200

## AIM
To create an aiming system (attach and aim a rifle with a character) in Unreal Engine,you’re using a third-person character and a rifle skeletal mesh.

## Procedure

### 1.Attach the Rifle to the Character

Import the Rifle Skeletal Mesh into Unreal Engine.
Open your Character Blueprint (e.g., BP_ThirdPersonCharacter).
In the Components tab:
Add a Skeletal Mesh or Static Mesh component (name it Rifle).
Set its Skeletal Mesh to your rifle asset.

### 2.Attach the Rifle to a socket on the character’s skeleton:

In the Rifle component, set the Parent Socket to something like hand_r (right hand socket).

manually attach in Event Graph:
```
Rifle->AttachToComponent(Mesh, FAttachmentTransformRules::SnapToTargetNotIncludingScale, "hand_rSocket");
```

### 3. Add Aiming Mechanism

Create a Boolean variable called IsAiming.
Set up Input in Project Settings:
Go to Edit > Project Settings > Input.
Add an Action Mapping named Aim (e.g., Right Mouse Button).

### 4. Adjust Camera When Aiming

Add a Camera Boom and Follow Camera.

In Event Graph:
```
When IsAiming = true, zoom the camera in (FOV) and slightly shift it over the shoulder.
```

## Output

![op1](https://github.com/user-attachments/assets/a0532d0d-65a9-4438-9061-328f456e1475)

![op2](https://github.com/user-attachments/assets/b30a3769-1323-4c9b-be1f-b8014aa13e0d)

##  Result
Attach Rifle with character mesh and implementation bullet spawn from Rifle is successfully done.
