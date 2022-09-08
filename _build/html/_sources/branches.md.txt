# Example Branches for References

There are 3 branches that connects Chronos with the web interface in the Chronos repository. This section will briefly describe each of the 3 branches.

1. `chronosweb_core`

This is the main and most updated Chronos-web branch. Since this is the most updated branch that contains all the core modules mentioned in the previous section, any form of Chronos-web development should be made with reference to this branch. Do study the previous section - [Core Modules for Development](core_design_principles) to properly understand how to develop your own Chronos-web branch based on the structure of `chronosweb_core`

2. `chronosweb_gt`

This branch was used primarily for testing and developing the core gui modules. For now, it only renders text regarding the auction stage that it is in, as well as the links between carriers and their customers. The groundwork has been layed for this branch, and it can be further developed by simply writing pygame code for each auction stage.  


3. `chronosweb_osmviz`

This branch was used to test the possibility of integrating the python library `osmviz` into the web interface. As it turns out, this is possible since the visualisations of `osmviz` is built with pygame. However, since the pygame code was written in the source code, the source code has been copied into this branch to be edited. When running `osmviz` functions, Chronos then refers to the directory containing the edited source code instead.


## Patching
As mentioned, only the branch `chronosweb_core` is the most updated. However, sometimes there is a need to patch all 3 branches together with the same code, since they all share the same web interface. Do look into using the following `git` command on the command line:

```python
# To patch file f from branch b into branch a
git checkout a # Ensure that you are in the receiving branch
git checkout --patch b f # Patch file f in branch a with that of branch b
```