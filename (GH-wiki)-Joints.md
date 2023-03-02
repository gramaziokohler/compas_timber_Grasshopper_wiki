# Joints

In `compas_timber` you can connect two `Beams` using one of the three types of joints: `T-Butt`, `L-Butt` and `L-Miter`.  

### Joint Topologies 

The prefixes in the joint names refer to how the two beams are positioned relatively to each other. We distinguish four (topological) situations: `I`, `L`, `T` and `X`:
* `I` - a splice, i.e. beams are co-linear and connect at their ends
* `L` - a corner, i.e. two beam meet at their ends at an angle
* `T` - one beam (here called _main beam_) connects with one of its ends along the length of the other (here called _cross beam_)
* `X` - the beams cross each other

<img src=https://user-images.githubusercontent.com/11560512/220873941-75faf74c-ceea-4999-aefb-c2e3e911055e.svg height = "100">

### Joint components

#### T-Butt
In a `T-Butt` joint, one beam (here called _main beam_) connects with one of its ends to the side of the other (here called _cross beam_). The side to connect to is selected automatically based on the angles between the main beam and the sides of the cross beam.  
<img src=https://user-images.githubusercontent.com/11560512/221683434-42d013e4-a875-48a7-8891-c37bb12fa75f.png height="100">

#### L-Butt
An `L-Butt` joint is similar to the `T-Butt` joint but additionally the cross beam is trimmed with the respective side of the main beam to create a clean corner joint.  
<img src=https://user-images.githubusercontent.com/11560512/221682027-030dbbe8-c844-4e13-b853-36c4aafcdd0f.png height = "100">

#### L-Miter
An `L-Miter` joint connects two beams with a planar cut at a bisector of an angle between them.  
<img src=https://user-images.githubusercontent.com/11560512/221681572-38556029-8ddb-41e3-9f34-dde1deb6b4fe.png height = "100">



### AutomaticJoint wizzard
Connecting beams can be automated using `JointCategoryRule` and `AutomaticJoints` components.  
`JointCategoryRule` component serves to define which joint type should be applied when a beam of the first category (`CatA`) meets a beam of the second category (`CatB`).  
`AutomaticJoints` component does two things: First, it determines if two beams connect and if yes, determines the joint topology (I, L, T or X). Then, assigns the join type to every connecting pair of beams according to the defined rules. If the defined joint type has a different topology than the beams, no joint is assigned (Example: two beams form a corner (L) but the rule tries to assign a T-Butt joint).
* `Beams`: list of beams. To avoid unintended results, it should be the same list that is later used as an input to `Assembly`
* `Rules`: rules defined using `JointCategoryRule` components
* `MaxDistance`: (optional) tolerance for finding connecting beams if the centerlines to not intersect exactly but are at a certain distance from each other.

<img src=https://user-images.githubusercontent.com/11560512/221694372-2d4e1a0f-346c-4772-8ca5-bbf0dcd20367.png height = "375">

***

[&larr; back to overview](https://github.com/gramaziokohler/compas_timber_Grasshopper_wiki)

