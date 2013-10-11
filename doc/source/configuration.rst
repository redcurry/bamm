Configuration
=============

Control File
------------

Configuration options and parameters in BAMM are specified in a *control file*,
a plain text file in which each line contains the name of the option or
parameter, an equal sign, and the value of the option or parameter::

    treefile = whaletree.tre
    runMCMC = 1

The path of the control file (relative to the current directory) is specified
with the flag ``-control`` when running bamm::

    ./bamm -control divcontrol.txt

Options and Parameters
----------------------

The following describes each configuration option and parameter for the
speciation-extinction component of bamm. For true/false values, use 1 for true
or 0 for false.

treefile
  The name of the input tree file (Newick format) to analyze.

sampleFromPriorOnly
  1 - run BAMM by sampling from prior only (ignoring likelihood
  contribution to posterior).
  0 - run full analysis.

runMCMC
  1 - run the MCMC sampler.
  0 - just check to see if data can be loaded correctly.

loadEventData
  *Description not yet available.*

eventDataInfile
  *Description not yet available.*

initializeModel
  Leave this as 1

useGlobalSamplingProbability
  1 - global correction for incomplete taxon sampling in likelihood
  calculation.

globalSamplingFraction
  Fraction (0.0 - 1.0) of the total number of species in the clade
  that are actually in the tree being analyzed.

updateLambdaInitScale

updateMuInitScale

updateLambdaShiftScale

updateMuShiftScale

updateEventRateScale

localGlobalMoveRatio
  MCMC tuning parameters. These are the "step sizes" for updating parameters
  during MCMC sampling.

minCladeSizeForShift
  *Description not yet available.*

lambdaInit0
  Starting speciation rate

lambdaShift0
  Starting rate change parameter for speciation (if 0, speciation rates
  won't change through time).

muInit0
  Initial extinction rate

muShift0
  *Description not yet available.*

targetNumber
  The expeced number of "events" or rate shifts on the tree,
  if there is no signal in the data.

lambdaInitPrior
  Mean of exponential distribution prior on speciation.

lambdaShiftPrior
  Pior on speciation rate change parameter.

muInitPrior
  Exponential prior on extinction.

muShiftPrior
  *Description not yet available.*

MeanSpeciationLengthFraction
  *Description not yet available.*

segLength
  *Description not yet available.*

mcmcOutfile
  The file name in which to write the MCMC parameter output

lambdaOutfile
  The file name in which to write branch-specific speciation
  rates.

muOutfile
  The file name in which to write branch-specific extinction rates.

acceptrateOutfile
  *Description not yet available.*

lambdaNodeOutfile
  *Description not yet available.*

eventWriteFreq
  *Description not yet available.*

treeWriteFreq
  Frequency (in generations) in which to write speciation/extinction rates.
  Recommended frequency of > 10000

mcmcWriteFreq
  *Description not yet available.*

eventDataWriteFreq
  *Description not yet available.*

acceptWriteFreq
  *Description not yet available.*

printFreq
  Frequency (in generations) in which to write to the screen.

NumberGenerations
  Number of MCMC generations.

updateRateEventNumber
  Frequency in which to update the number of events (shifts) on the
  tree.

updateRateEventPosition
  Frequency in which to move the position of a shift point.

updateRateEventRate
  Frequency in which to update the rate at which events occur.

updateRateLambda0
  Frequency in which to update the initial speciation rate for an
  event.

updateRateLambdaShift
  Frequency in which to update how speciation rates change through
  time.

updateRateMu0
  Frequency in which to update the initial extinction rate.

initialNumberEvents
  *Description not yet available.*

