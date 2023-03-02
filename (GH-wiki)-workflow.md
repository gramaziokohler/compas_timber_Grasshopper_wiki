# Workflow

To build a timber frame `Assembly`, you need to:
* create `Beams`
* define `Joints` between these beams
* define other `Features` (optional)  

Based on this, `Assembly` takes care of generating the final geometry of the structure.

<img src=https://user-images.githubusercontent.com/11560512/221904983-faa82f7d-7603-4941-bda3-9543f04a14dc.png height=200>


&nbsp;&nbsp;

**Example:**   

<img src=https://user-images.githubusercontent.com/11560512/221913009-986bcb06-6a20-46e5-b917-706fbaf55ebb.png height=200>


&nbsp;

**Important!**   

* The order in the list of `Joints` and `Features` matters! For example: if there are two different joints defined for the same pair of beams in the list, the last one will be applied (overrides entries earlier in the list).
* The `Joints` are processed first, then `Features`.



***

[&larr; back to overview](https://github.com/gramaziokohler/compas_timber_Grasshopper_wiki)

