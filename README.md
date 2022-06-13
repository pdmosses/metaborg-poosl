# Spoofax Language Workbench implementation for POOSL

POOSL is an abbreviation of Parallel Object-Oriented Specification Language. This language originates from research at Eindhoven University of Technology:
* P.H.A. van der Putten, and J.P.M. Voeten, "Specification of Reactive Hardware/Software Systems: The Method Software/Hardware Engineering (SHE)", Ph.D. thesis, Eindhoven University of Technology, 1997. https://doi.org/10.6100/IR491299
* L. van Bokhoven, "Constructive Tool Design for Formal Languages; From Semantics to Executing Models", Ph.D. thesis, Eindhoven University of Technology, 2004. https://doi.org/10.6100/IR559665

The main toolset for POOSL consists of textual and graphical editors, a command-line simulator, and an interactive debugging environment; this toolset is available at https://www.poosl.org/

This partial Spoofax implementation provides an incomplete textual editor. The type checker is documented in the following article:
* A.J. Mooij, "Static type checking without downcast operator", Information Processing Letters, Volume 178, November 2022. https://doi.org/10.1016/j.ipl.2022.106285

Educational POOSL examples can be downloaded from https://github.com/eclipse/poosl/tree/main/plugins/org.eclipse.poosl.ide.examples/content
Note that only the following example works out-of-the-box in the partial Spoofax implementation:
* org.eclipse.poosl.examples/models-basic/Jobshop/jobshop.poosl
