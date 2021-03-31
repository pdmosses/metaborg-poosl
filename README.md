# Spoofax Language Workbench implementation for POOSL

POOSL is an abbreviation of Parallel Object-Oriented Specification Language. This language originates from research at Eindhoven University of Technology:
* P.H.A. van der Putten, and J.P.M. Voeten, "Specification of Reactive Hardware/Software Systems: The Method Software/Hardware Engineering (SHE)", Ph.D. thesis, Eindhoven University of Technology, 1997. https://doi.org/10.6100/IR491299
* L. van Bokhoven, "Constructive Tool Design for Formal Languages; From Semantics to Executing Models", Ph.D. thesis, Eindhoven University of Technology, 2004. https://doi.org/10.6100/IR559665

The main toolset for POOSL consists of textual and graphical editors, a command-line simulator, and an interactive debugging environment; this toolset is maintained by [ESI (TNO)](https://esi.nl/) and can be obtained from: https://poosl.esi.nl/

This partial Spoofax implementation provides an incomplete textual editor. A bundle with educational POOSL examples can be downloaded from http://poosl.esi.nl/downloads/examples/examples-latest.zip
Note that only the following example works out-of-the-box in the partial Spoofax implementation:
* nl.esi.poosl.examples/models-basic/Jobshop/jobshop.poosl
