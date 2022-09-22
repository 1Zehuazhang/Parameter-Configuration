# Parameter-Configuration
This file contains the calculated parameters for McVol and Rosetta_cartesian_ddg 
--------------------------------------------------------------------------------
Detailed parameters for McVol: 
nmc 250       ! Number of Monte Carlo steps per A3 molecule
surfPT 2500    ! Number of surface points per atom
probe 1.1     ! Probe sphere radius
membZmin -10  ! Minimum Z coordinate for the membrane
membZmax 10   ! Maximum Z coordinate for the membrane
startgridspacing 1.0   ! Grid spacing fo the initial search
membgridspacing 2.0    ! Grid spacing for the membrane
cavgridspacing 0.5     ! Grid spacing for the cavity refinement
minVol 7       ! Minimum volume for cavities to be treated
waterVol 18     ! Volume of one water molecule
DummyRad 1.7    ! Radius of the dummy atoms placed as membrane
blab 0          ! Output level
MembDim 4      ! Thickness of the membrane in x/y direktion
CoreZMin 0     ! Membrane Core region minimum Z coordinate
CoreZMax 0      ! Membrane Core region maximum Z coordinate
CoreDim 0       ! Allowed distance of membrane points not in core region
CleftDim 3     ! Kind of a inverse probe sphere radius for a cleft
CleftRel 70
CleftMethod 2
SurfaceCluster 1.5

--------------------------------------------------------------------------------
Detailed parameters for cartesian_relax_flags: 
-nstruct 10
-ex1
-ex2
-use_input_sc
-flip_HNQ
-no_optH false
-relax:cartesian
-score:weights ref2015_cart
-crystal_refine

--------------------------------------------------------------------------------
Detailed parameters for cartesian_ddg_flags:
-ddg:mut_file mtg_saturation.mutfile
-ddg:iterations 3
-ddg:cartesian
-ddg::dump_pdbs False
-bbnbrs 1
-fa_max_dis 9.0
-score:weights ref2015_cart
-relax:cartesian
-relax:min_type lbfgs_armijo_nonmonotone
-ex1
-ex2
-use_input_sc
-flip_HNQ
-optimization:default_max_cycles 200
-crystal_refine
