# Spoofax Language Workbench implementation for POOSL

POOSL is an abbreviation of Parallel Object-Oriented Specification Language. This language originates from research at Eindhoven University of Technology:
* P.H.A. van der Putten, and J.P.M. Voeten, "Specification of Reactive Hardware/Software Systems: The Method Software/Hardware Engineering (SHE)", Ph.D. thesis, Eindhoven University of Technology, 1997. https://doi.org/10.6100/IR491299
* L. van Bokhoven, "Constructive Tool Design for Formal Languages; From Semantics to Executing Models", Ph.D. thesis, Eindhoven University of Technology, 2004. https://doi.org/10.6100/IR559665

The main toolset for POOSL consists of textual and graphical editors, a command-line simulator, and an interactive debugging environment; this toolset is available at https://www.poosl.org/

This partial Spoofax implementation of POOSL provides an incomplete textual editor. The type checker is documented in the following article:
* A.J. Mooij, "Static type checking without downcast operator", Information Processing Letters, Volume 178, November 2022. https://doi.org/10.1016/j.ipl.2022.106285

To install this partial Spoofax implementation of POOSL:
* Install Spoofax
* Import these Maven projects into Spoofax: File -> Import... -> Maven -> Existing Maven Projects

Educational POOSL examples can be downloaded from https://github.com/eclipse/poosl/tree/main/plugins/org.eclipse.poosl.ide.examples/content
Note that only the following example works out-of-the-box in the partial Spoofax implementation:
* org.eclipse.poosl.examples/models-basic/Jobshop/jobshop.poosl

## Hyperlinked twin website

> Added by @pdmosses

The following files and directories have been added to this fork,
to support the generation of a [hyperlinked twin website]
with precise name-based code navigation and highlighting:

- `docs/`
- `mkdocs.yml`
- `.github/workflows/ci.yml`

[hyperlinked twin website]: https://pdmosses.github.io/metaborg-poosl/

### Local preview

The following commands build and serve a local preview of the generated website:

```sh
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install mkdocs-material
pip install mkdocs-awesome-pages-plugin
mkdocs serve
```

When a new commit is pushed to either the `master` or `main` branches,
the hyperlinked twin website site is automatically built and deployed on GitHub Pages.
 
### Changed files

To preserve the alignment of the code in the generated web pages,
all tab characters in the SDF3 and Statix files have been expanded to spaces.

The shell commands used in the `syntax` and `trans` directories were:

```sh
find ./ -name '*.sdf3' -type f -exec bash -c 'expand -t 4 "$0" | sponge "$0"' {} \;
find ./ -name '*.stx' -type f -exec bash -c 'expand -t 4 "$0" | sponge "$0"' {} \;
```
