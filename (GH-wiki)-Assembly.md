# Assembly
`Assembly` component creates a frame structure made of joined `Beams`. It connects the beams and adds features based on provided `Joints` and `Features` definitions. 

Geometric operations like cutting, trimming and solid boolean subtractions, which are implied by joints and features, may be computationally expensive, and are disabled by default. To activate it, set `applyFeatures` to `True`. `Errors` provide a log of unsuccessful feature-apply operations. 


Assembly as such is an abstract object. To visualize it (to visualize the beams in the assembly), use the `ShowAssembly` component that returns the _Brep_ geometry of the beams. 

<img src=https://user-images.githubusercontent.com/11560512/221914346-ccdfcda1-d47f-4e1e-9192-9b22f8de20d1.png height=100>


***

[&larr; back to overview](https://github.com/gramaziokohler/compas_timber_Grasshopper_wiki)
