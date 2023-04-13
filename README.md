# PavlovVR-BipodComponent

# Add Components
1. Add the Component "CMP_Bipod" to your gun.
2. Add two SkeletalMeshComponents to your gun. Name one "Bipod" and the other one Hand. (names dont matter, makes it easier to use)
3. Set the "Bipod" SkeletalMeshComponent to Component Replicates = True.
4. Add a trigger for the Bipod. This can be an InteractBox or pretty much anything.

# Setup the BipodComponent
## ConstructionScript
![grafik](https://user-images.githubusercontent.com/84019236/231751396-3235186a-0ec4-410e-b61b-857ced48ce52.png)
1. Run the "ConstructionScript" function of the BipodComponent.
2. Connect the variables as seen in the image.
3. Write the names of the Root and Bipod bone into the name variables.
4. Bipod Length: The Bipod Length is the length that the bipod has when extended/in use to the ground. (red line)
![grafik](https://user-images.githubusercontent.com/84019236/231220768-65f4c105-d0f7-426f-b926-f6a26af8bbca.png)
You need to calculate that length yourself. There are triangle calculator websites if you dont know how to do calculate it yourself.
5. Max Distance to Grip. That is the distance on how far your controller can be away from the hand that is attached to the gun. If that value is exceeded it will deactivate the bipod and but the gun back in your hand/controller.
6. Circular Angle Limit: That limits the movement of the gun when the bipod is active in a circular area. Value in Degrees. Leave it at 0 if you want to use the default rectangular limit.
7. Up/Down Left/Right Limit. That limits the movement of the gun when the bipod is active in a rectangular area. Value in Degrees. These values will always be used if the Circular Angle Limit = 0.

## EventGraph
![grafik](https://user-images.githubusercontent.com/84019236/231223236-9b4b2cf1-475d-4c46-ae89-d6423c6b6830.png)

Just run the events/set the variables as in the image shown. This example uses an interact box to trigger the bipod.

# The Bipod Mesh/AnimBP
The BipodMesh needs to be an SkeletalMesh and has to be seperate from the gun. The IsBipodActive? variable of the BipodCmponent can be used to trigger the animation(s) in the Animation Blueprint for the BipodMesh.



### Dm me if you have any questions,... on Discord. [DarkAt26#7075]

### Special thanks to KENNITHH for his help/testing.
