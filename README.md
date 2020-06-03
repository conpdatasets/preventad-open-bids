# PREVENT-AD open Dataset organized according to the BIDS standard

### Overview

This is a derived dataset of `preventad-open` where all the images are organized according to the BIDS standard. Conversion to NIfTI was performed from the original MINC files available in the `preventad-open` dataset.

The PREVENT-AD (Pre-symptomatic Evaluation of Experimental or Novel Treatments for Alzheimer Disease) cohort is composed of cognitively healthy participants over 55 years old, at risk of developing Alzheimer Disease (AD) as their parents and/or siblings were/are affected by the disease. These ‘at-risk’ participants have been followed for a naturalistic study of the presymptomatic phase of AD since 2011 using multimodal measurements of various disease indicators. Two clinical trials intended to test pharmaco-preventive agents have also been conducted.

The PREVENT-AD research group is now releasing data openly with the intention to contribute to the community’s growing understanding of AD pathogenesis.

More detailed information about the study design can be found in the LORIS instance of Open PREVENT-AD (https://openpreventad.loris.ca).

### Data organization

Data are organized according to the BIDS standard in the `BIDS_dataset` directory. Specifications of the BIDS standard are available [here](https://bids-specification.readthedocs.io/en/stable/).

```
preventad-open
|__DATS.json
|__BIDS_dataset
   |__dataset_description.json
   |__participants.json
   |__participants.tsv
   |__README
   |__sub-<candidate_id>
      |__ses-<visit_label>
            |__sub-<candidate_id>_ses-<visit_label>_scans.json
            |__sub-<candidate_id>_ses-<visit_label>_scans.tsv
                  |__anat
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.nii.gz
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.json
                        ...
                  |__asl
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.nii.gz
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.json
                        ...
                  |__dwi
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.nii.gz
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.json
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.bval
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.bvec
                        ...
                  |__fmap
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.nii.gz
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.json
                        ...
                  |__func
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.nii.gz
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>.json
                        |__ sub-<candidate_id>_ses-<visit_label>_run-<number>_<BIDS_scan_type>_events.txt
                        ...
```

- `DATS.json` is a JSON file that describes the content of the dataset

### For more information: 

- LORIS open database instance with the PREVENT-AD dataset: https://openpreventad.loris.ca
- PREVENT-AD study web site: https://prevent-alzheimer.net/
- PREVENT-AD Twitter account: https://twitter.com/prevent_ad
- Dataset DOI: https://doi.org/10.5281/zenodo.3875552
