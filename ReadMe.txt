
===============================================================
GFSSP-Generalized Fluid System Simulation Program WINDOWS-PORT:
===============================================================

GFSSP, v1.4.1, Generalized Fluid System Simulation Program to model flow distribution in fluid networks, ported to WINDOWS OS.

GFSSP is a general purpose computer program for analyzing flow and pressure distribution in a complex network. The program is capable of modeling phase changes, compressibility, mixture thermodynamics and external body forces such as gravity and centrifugal.

1. Pre-Requisits/Reference:

1a. Additional reference materials located at: https://www.nasa.gov/gfssp/related-material


2. Documentation:

2a. User's Guide located in "./GFSSP_v1.4_USERS_GUIDE.pdf"


3. Example problems are located in "./examples/":


4. Example problem: "EXAMPLE1" located in "./examples/ex1/":
4a. INPUT FILES: "EXAMPLE1.DAT".

==================================
START: Input File: "EXAMPLE1.DAT"
==================================
TITLE
Case 1
DENCON        GRAVITY       ENERGY        MIXTURE       THRUST        STEADY        TRANSV
F             T             T             F             F             T             F
INERTIA       CONDX         TWOD          PRINTI        ROTATION      BUOYANCY      HRATE
T             F             F             F             F             F             F
NNODES        NINT          NBR           NF            NHREF
 16            14            15            1             2 
RELAXK        RELAXD        RELAXH
 1             0.5           1 
NFLUID(I), I=1,NF
     11     
NODE          INDEX
 1             2 
 2             1 
 3             1 

...<content removed> ...

BRANCH
 1516 
UPSTREAM ANGLE
 1415         0.0000
DOWNSTREAM ANGLE
==================================
START: Input File: "EXAMPLE1.DAT"
==================================


5. Operation: Run "./bin/gfssp1p4.exe"


6. OUTPUT FILES: "example1.out", & "GFSSP.OUT".


==================================
START: Output File: "example1.out"
==================================
  **** GENERAL FLUID SYSTEM SIMULATION PROGRAM ****
  ****************** VERSION 1.4.1 ****************
   
  TITLE     :Case 1                                                                          
  DATE      :10/13/18       
  ANALYST   :Joe Blow                      
  FILEIN    :EXAMPLE1.DAT   
  FILEOUT   :example1.out   
   LOGICAL VARIABLES

... <content removed> ...

 BRANCHES
 BRANCH       KFACTOR       DELP        FLOW RATE VELOCITY   REYN. NO.   MACH NO
 .
       (LBF-S^2/(LBM-FT)^2) (PSI)      (LBM/SEC)     (FT/SEC)
    12       0.631E-05     0.242E-01   0.800E+03     0.251E+01   0.529E+06   0.209E-02
    23       0.989E-06     0.439E-02   0.800E+03     0.251E+01   0.529E+06   0.209E-02
    34       0.300E-05     0.818E-02   0.800E+03     0.251E+01   0.529E+06   0.209E-02
    45       0.000E+00     0.000E+00   0.800E+03     0.251E+01   0.529E+06   0.209E-02
    56       0.194E-04     0.478E-01   0.800E+03     0.251E+01   0.529E+06   0.209E-02
    67       0.881E-05     0.276E+00   0.800E+03     0.459E+01   0.716E+06   0.383E-02
    78       0.562E-04     0.224E+00   0.800E+03     0.459E+01   0.716E+06   0.383E-02
    89       0.479E-02     0.213E+02   0.800E+03     0.459E+01   0.716E+06   0.383E-02
   910       0.562E-04     0.224E+00   0.800E+03     0.459E+01   0.716E+06   0.383E-02
  1011       0.667E-05    -0.881E-02   0.800E+03     0.251E+01   0.529E+06   0.209E-02
  1112       0.194E-04     0.478E-01   0.800E+03     0.251E+01   0.529E+06   0.209E-02
  1213       0.627E-03     0.279E+01   0.800E+03     0.251E+01   0.529E+06   0.209E-02
  1314       0.648E-05     0.159E-01   0.800E+03     0.251E+01   0.529E+06   0.209E-02
  1415       0.198E-05     0.880E-02   0.800E+03     0.251E+01   0.529E+06   0.209E-02
  1516       0.108E-04     0.104E+02   0.800E+03     0.251E+01   0.529E+06   0.209E-02


  SOLUTION SATISFIED CONVERGENCE CRITERION OF  0.00100 IN   21 ITERATIONS
==================================
END: Output File: "example1.out"
==================================



