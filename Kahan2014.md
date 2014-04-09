#Kahan et al - Resting State Functional MRI in Parkinson's disease: the impact of deep brain stimulation on 'effective' connectivity

## Introduction
* PD: progressive degeneration of nigrostriatal innervation
* Deep brain Stimuluation is therapy when dopamenergic medication no longer
  works
  * Mechanism less well understood than the medication
  * Originally it was suggested that DBS works as a lesion, inhibiting the
    target.
  * Literature suggests that "a Myriad of effects culminates in clinical
    improvement.

* Parkinsonian patients off medication show fucntional connectivity:
  * pre/motor cortex -> putamen - reduced
  * M1 -> cerrebellum - increased
  * striatum -> thalamus - reduced
  * M1 -> STN - increased
 * "Wealth of evidence implicating dopamine's role in resting
   cortico-subcortical circuits."
* Earlier PET studies have shown changes in blood flow and glucose metabolism
  in M1, putamen and thalamus as a result of DBS.
* Functional MRI in DBS patients is problematic due to safety issues.

### Dynamic causal modeling
 * way to infer connectivity of different areas.
 * _Stochastic_ DCM is suited for resting state data
   * assumes stochastic fluctuations that drive larger fluctuations in
     entire system

### This study
Use DCM and resting state data in DBS-patients to observe effects in
underlying effective connectivity.

Hypothesis: DBS has a modulatory effect on 'extrinsic' connectivity in the
motor loop, as opposed to a global effect.

Additionally: can clinical measures of PD be explained by these
connectivity measures?

## Materials and methods
### Patients
* n=12
* STN DBS for > 6 months
* Medication was withdrawn 10-12 houurs before scanning

### MRI
 * 1.5T
 * TR = 2420ms
 * resolution = 3x3x4.2mm
 * Three blocks:
   1. Rest
   2. Motor task (right)
   3. Motor task (left)
 * Motor task consisted of moving joystick in random direction when subject
   heard a tone.
 * The motor task was used as a fuctional localizer (M1)
 * Resting state scan was repeated twice, once ON DBS, once OFF DBS.

### DCM
* DCM is a model of interconnected nodes.
  * Bayesian model selection
    * Tradeoff between model accuracy and model complexity.
* Original model was 'deterministic'
* Extension to 'stochastic' DCM was nescessary to account for 'endogenous'
  activity.

* Hypothetocal networks were built, including the following nodes:
  1. M1
  2. Putamen
  3. Motor thalamus
  4. STN (hidden)

Hemispheres are treated seperately, because:
 1. PD causes assymetric degeneration of SN
 2. Severity of motor symptoms is usually assymetric.
 3. DBS settings are usually assymetric


### Functional Localization of M!
Peak voxel of motor task contrast within predefined precentral gyrus,
contralateral to hand movement was considered as M1 coordinate.

### Preprocessing
* removal first 5 scans
* Normalized to MNI
* 8mm FWHM smoothing
* Sessions were concatenated

### GLM of resting state dynamics
Regressors:
 * 189 cosine functions, representing frequencies characteristic of resting
   state dynamics (0.0078 - 0.1Hz)A
 * Regressor encoding effect of DBS
 * Six motion regressors
 * Two confound regressors recorded in eyeball and lateral ventricle

M1 signal wasextracted by using a F-contrast including the
stimluation-regresor, as well as the cosine regressors.

This signal was PPI'd with putamen and thalamus masks.

### Model space
GPe and GPi are not modeled, there place in direct and indirect pathway are
modeled as direct directions from striatum to thalamus and STN to thalamus
respectively.

Model was fit using generalized filtering, a Bayesian technique to fit
models with latent variables (solves inversion problem).

### Relationship between winning dynamic causal modelling and clinical response to deep brain stimulation
Connection strengths were related to UDPRS-score.

## Results
### Patients


### Model fit
Model did not fit in two subjects, but did after rescaling.

### Bayesian Model Selection
Model 32 was most likely: a modulatory effect of DBS on *all* pathways.

### Direction of neuromodulatory effect
* Increased connectivity as result of DBS:
  * Cortico-striatal
  * Direct pathway
  * thalamo-cortical pathway
* Decreases connectivity as result of DBS:
  * All pathways including STN:
    * hyperdirect
    * Striatum -> STN
    * STN -> thalamus

### Strenghth of connection predicts clinical impairment
 * Reduced clinical impairment when:
   * stronger direct pathway
   * hyperdirect pathway
 * Increased clinical impairment when:
   * striato-STN pathway

### Change in connection strengths predict clinical efficacy
Amount of change in abovementioned pathways predict clinical efficacy (but
no too much).

## Discussion
### Widespread neuromodulation
### Enhanced thalamic sensitivity to the direct pathway
Direct pathway is stronger under DBS and reduces symptoms.

### Subthalamic nucleus afferents and deep brain stimulation
"The role of the hyperdirect remains unclear."


In the literature, stronger hyperdirect pathways usually lead to increased
severity of symptoms, in this tudy this is reversed.

Strength of the indirect pathway was less able to predict these results.
The effect was in the expected direction though.

Most of the STN-DBS literature focused on regional activity and not so much
connections. They conclude mostly that DBS increases thalamic activity, but
reduces cortical motor activity.

### Limitations and model assummptions
Assumptions:
 * independence of left and right hemisphere
 * DBS modulates activity in entire functional motor loop.
 * Lack of pallidal nodes

## Conclusion
Hyperdirect, direct and STN afferents arising from the striatum are the
most important predictors of clinical improvement.

Therapeutic effects might be induced by making STN less susceptible to
input STN and making thalamus more susceptible to direct pathway input.

The hyperdirect pathway has the reverse effect. STN DBS maybe has a
negative influence on clinical outcome by strengthening the hyperdirect
pathway.

This paper shows how advanced methodological inventions can help clinical
research in mechanistic understanding of disease.


