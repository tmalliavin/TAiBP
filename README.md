# TAiBP
Threading-augmented interval Branch-and-Prune

The interval Branch-and-Prune (iBP) approach, based on the reformulating of the
Distance Geometry Problem (DGP) provides a theoretical frame for the generation
of protein conformations, by systematically sampling the conformational space.
When an appropriate subset of inter-atomic distances is known exactly,
this worst-case exponential-time algorithm is provably complete and
fixed-parameter tractable. These guarantees, however, quickly
disappear as distance measurement errors are introduced.

An implementation of the approach iBP, developed by Bradley Worley, is available 
in the repository ibp-ng. The initial ibp-ng github depository is: 
https://github.com/geekysuavo/ibp-ng

An improvement of the approach iBP: the threading-augmented interval Branch-and-Prune
(TAiBP), was proposed in:

Malliavin TE, Mucherino A, Lavor C, Liberti L. Systematic Exploration of Protein
Conformational Space Using a Distance Geometry Approach. J Chem Inf Model. 2019
Oct 28;59(10):4486-4503. doi: 10.1021/acs.jcim.9b00215.

where the combinatorial explosion of the original iBP approach arising from its
exponential complexity is alleviated by partitioning the input instances into
consecutive peptide fragments and by using Self-Organizing Maps (SOMs)
to obtain clusters of similar solutions. The representative conformations
of the fragments obtained from the clustering are then assembled to build the
protein structure.

The initial github depository for Self-Organizing Maps, was developed by Guillaume 
Bouvier at: https://github.com/bougui505

The calculation inputs are: a uniform covalent geometry extracted from force field
covalent terms, the backbone dihedral angles with error intervals.

## Available archives

The python scripts for running TAiBP are contained in the archive TAiBP.tgz,

The python scripts for using Self-Organizing Maps (SOMs) are in the archive SOM.tgz.

## Note that the python scripts are written in python 2! 

The archive example_run.tg contains an example of running iBP and clustering for
a peptide fragment (seg_2_11) and of running the assembly of two fragments (make_glue).

## Licensing

This project is released under the
[MIT license](https://opensource.org/licenses/MIT). See the
[LICENSE.md](LICENSE.md) file for the complete license terms.
