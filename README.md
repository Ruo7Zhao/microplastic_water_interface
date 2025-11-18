# microplastic_water_interface
Example analysis scripts for the accompanying manuscript on hydroxide hydrogen-bonding
and interfacial water structure at water–polymer interfaces. Scripts are provided as
Jupyter notebooks in the directories listed below, together with short example
trajectories.

./calculate-hbond
    Contains scripts and example data used to analyze the probability distribution
    of OH⁻ hydrogen-bond numbers.

    - H-bond_distribution.ipynb
        Jupyter notebook that loads the example trajectory (water-PE.dcd / water-PE.pdb),
        identifies hydrogen bonds formed by OH⁻, and computes the probability distribution
        of the number of H-bonds per OH⁻. The notebook also demonstrates how to
        restrict the analysis to interfacial regions (e.g., within a given distance
        from the Gibbs dividing surface).

    - water-PE.pdb / water-PE.dcd
        Short example trajectory of a water–PE system used to demonstrate the
        hydrogen-bond analysis workflow.

./calculate-structure-properties
    Contains scripts and example data used to analyze interfacial structural
    properties, including dangling OH groups and local order parameters (q₃ and q₄),
    for water at a polymer interface.

    - dangling-OH.ipynb
        Jupyter notebook that identifies interfacial water molecules and computes
        the fraction and spatial distribution of dangling OH groups as a function
        of distance from the Willard-Chandler Interface (WCI).

    - q3.ipynb / q4.ipynb
        Jupyter notebooks that compute and analyze the q₃ and q₄ orientational
        order parameters for interfacial water, using the example trajectory
        (water_PMMA.dcd / water_PMMA.pdb). The notebooks produce profiles and
        summary statistics, and save intermediate results in .csv and .npz formats
        (see q3_meta.json and q4_meta.json for binning metadata).

    - water_PMMA.pdb / water_PMMA.dcd
        Short example trajectory of a water–PMMA system used to demonstrate the
        dangling-OH and order-parameter analyses.

All notebooks are intended to be run from within their respective directories.
They are written for Python 3 and rely on standard scientific Python packages
(e.g., NumPy, MDTraj/MDAnalysis, Matplotlib). Please see the 
environment file "environment.yml" for details on the software dependencies and installation
instructions.
