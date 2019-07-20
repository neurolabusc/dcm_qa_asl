
## About

dcm_qa_asl is a simple DICOM to NIfTI validator script and dataset to test conversion of Siemens [arterial spin labeling](https://www.mccauslandcenter.sc.edu/crnl/tools/asl) images. Specifically, recent versions of dcm2niix attempt to extract relevant ASL settings from the [proprietary CSA header](https://nipy.org/nibabel/dicom/siemens_csa.html). These settings are critical for analyzing ASL data using tools like [BASIL](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/BASIL) or [ASLtbx](https://cfn.upenn.edu/~zewang/ASLtbx.php).

The provided datasets are intentionally incomplete: only a couple volumes of data are provided and auxiliary files (M0/PD images) are not provided. The intention of this repository is to detect accurate conversion of sequence specific tags. Users interested in full sample datasets can visit [osf.io](https://osf.io/td4bx/) or acquire the [BASIL example datasets](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/BASIL).

## DataSets

* PASL2D
  * Description: 2D Siemens product pulsed-ASL
  * Sequence: ep2d_pasl
  * Sequence Specific Tags: InversionTime, SaturationStopTime

* PASL3D
  * Description: 2D Siemens product pulsed-ASL
  * PulseSequenceDetails: ep2d_pcasl
  * Sequence Specific Tags: BolusDuration, InversionTime

* pCASL2D
  * Description: [2D loft labpseudocontinuous ASL ](http://www.bmap.ucla.edu/about/peopledetails/danny_wang/)
  * PulseSequenceDetails: ep2d_pcasl
  * Sequence Specific Tags: LabelOffset, PostLabelDelay, NumRFBlocks, RFGap, MeanGzx10, PhiAdjust

* pCASL3D
  * Description: [3D loft labpseudocontinuous ASL ](http://www.bmap.ucla.edu/about/peopledetails/danny_wang/)
  * Sequence: tgse_pcasl
  * Sequence Specific Tags: RFGap, MeanGzx10, T1

* pCASL2Dve
  * Description: [3D vessel-encoded pseudocontinuous ASL](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3824178/)
  * Sequence: ep2d_VEPCASL
  * Sequence Specific Tags: InversionTime, BolusDuration, TagRFFlipAngle, TagRFDuration, TagRFSeparation, MeanTagGradient, TagGradientAmplitude, TagDuration, MaximumT1Opt, InitialPostLabelDelay(s)
  * Source: [osf.io](https://osf.io/td4bx/)

* pCASL3Dve
  * Description: [3D vessel-encoded pseudocontinuous ASL](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3824178/)
  * Sequence: tgse_VEPCASL
  * Sequence Specific Tags: TagRFFlipAngle, TagRFDuration, TagRFSeparation, MaximumT1Opt, Tag0, InitialPostLabelDelay(s), TagPlaneDThickness
  * Source: [osf.io](https://osf.io/td4bx/)
