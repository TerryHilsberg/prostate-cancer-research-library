# AI and Integrated Test Decision Support in Prostate Cancer: Evidence Map

Retrieved: **2026-07-17**  
Category: **Imaging & Biomarkers; Risk Stratification & Staging; Diagnostic Workup; Localized Treatment; Shared Decision-Making**  
Scope: approaches that combine PSA, clinical variables, mpMRI, biopsy/pathology, genomic tests, and PSMA PET/CT to guide prostate cancer diagnosis, risk stratification, treatment selection, and local-treatment targeting.

!!! warning "Not medical advice"
    This page summarizes decision-support evidence for education and clinician discussion. AI models, risk calculators, radiomics tools, genomic classifiers, and imaging-fusion systems should not replace specialist interpretation by urologists, radiation oncologists, radiologists, nuclear medicine physicians, pathologists, and medical oncologists. Many AI tools are promising but still require external validation, workflow integration, calibration to local populations, and proof that using them improves patient outcomes.

## Patient-facing bottom line

| Decision point | What is already used | What AI/integrated tools are adding | Main caution |
|---|---|---|---|
| **Should I have a biopsy?** | PSA, PSA density, DRE, family history, age, prior biopsy, prostate volume, mpMRI/PI-RADS, risk calculators and biomarkers. | MRI-based risk calculators, blood-test + MRI pathways, and emerging MRI+PSMA PET calculators can reduce unnecessary biopsies and target clinically significant cancer. | A “low-risk” calculator result is not a diagnosis; missed clinically significant cancer remains possible. |
| **Where should biopsy target?** | mpMRI-visible lesions with MRI/US fusion or in-bore biopsy; systematic cores remain important. | AI lesion detection, prostate/lesion segmentation, and MRI+PSMA PET fusion may improve consistency and targeting. | AI can miss lesions or overcall artifacts; systematic/template sampling may still be needed. |
| **How aggressive is the cancer?** | Grade Group/Gleason score, tumour volume/core involvement, PSA/PSA density, MRI stage, clinical stage, genomic classifiers. | Digital pathology AI and multimodal AI can quantify histology and combine pathology with clinical variables to predict recurrence/metastasis or treatment benefit. | Many models are retrospective; clinical-use thresholds and equity/generalizability require validation. |
| **Is cancer still localized?** | mpMRI for local extent; PSMA PET/CT for staging selected intermediate/high-risk disease and recurrence; CT/bone scan in older pathways. | PSMA PET + MRI/radiomics models may better define intraprostatic lesions, nodal disease, and radiation targets. | PSMA PET is not perfect for microscopic nodal disease and should not replace biopsy/pathology. |
| **Can local treatment be targeted?** | mpMRI-defined dominant intraprostatic lesion; biopsy map; focal therapy planning; radiation boost planning. | AI segmentation/radiomics and PSMA PET/MRI fusion may help define dominant lesions, ablation margins, focal radiation boost volumes, and biologically targeted radiotherapy. | Registration error, MRI-invisible disease, PSMA-negative tumour, and multifocal disease can undermine focal plans. |
| **Which treatment intensity is needed?** | NCCN/EAU risk groups, nomograms, Decipher/other genomic classifiers, clinician judgment. | AI pathology and multimodal models are being developed to predict who benefits from ADT duration, salvage therapy, or intensification. | Predictive AI is different from prognostic AI; few tools have prospective outcome-changing validation. |

## Integrated-data approaches covered

1. **Traditional clinical risk calculators and nomograms** — PSA, age, DRE, family history, prostate volume, prior biopsy, biopsy Grade Group, stage.
2. **MRI-enhanced biopsy risk calculators** — add PI-RADS, lesion size/location, prostate volume, PSA density.
3. **Blood/biomarker + MRI pathways** — Stockholm3, Proclarix, PHI/4K-like strategies, genomic tissue classifiers.
4. **PSMA PET + MRI risk calculators** — emerging tools combining clinical variables, mpMRI, and PSMA PET/CT before biopsy or for staging.
5. **AI/radiomics for mpMRI and PSMA PET** — lesion detection, segmentation, grade prediction, extracapsular extension prediction, dominant-lesion mapping.
6. **Digital pathology AI** — biopsy/prostatectomy slide analysis for Gleason grading, tumour quantification, recurrence/metastasis risk, and treatment-benefit prediction.
7. **Multimodal AI** — combines clinical data, digital pathology, imaging, and sometimes genomic/molecular information.
8. **Local-treatment targeting systems** — MRI/US fusion biopsy, PSMA PET/MRI registration, radiomics-guided focal boost, focal therapy planning, ablation-margin planning.

## Clinical workflow: where integration happens

### 1. Before biopsy: biopsy decision and target selection

The mature decision-support layer is not necessarily “AI” in the modern deep-learning sense. Many tools are statistical risk calculators that combine PSA, age, DRE, family history, prostate volume, prior biopsy, and now MRI findings. These help estimate the probability of any prostate cancer and clinically significant prostate cancer.

The current direction is to combine:

- PSA and PSA density;
- age, DRE, family history, prior biopsy;
- prostate volume;
- mpMRI PI-RADS score and lesion features;
- blood biomarkers such as Stockholm3, PHI/4K-like tests, Proclarix;
- in selected settings, PSMA PET/CT.

**Patient-facing interpretation:** these tools can help decide whether biopsy is needed and where to target it, but a negative MRI or low calculator score does not guarantee absence of significant cancer.

### 2. At biopsy: mapping the prostate

MRI-targeted biopsy improves sampling of visible lesions, but focal treatment and treatment targeting require more than “a positive biopsy.” The team needs to know:

- which lesion is the index lesion;
- whether contralateral or out-of-field clinically significant cancer exists;
- whether MRI-visible disease matches biopsy grade and location;
- whether systematic or template cores show hidden disease;
- whether PSMA PET uptake corresponds with the MRI lesion or reveals MRI-invisible disease.

AI can assist by segmenting prostate zones and lesions, flagging suspicious regions, and creating 3D maps, but final targeting still depends on expert imaging and pathology review.

### 3. After diagnosis: risk stratification and treatment intensity

Standard prostate cancer risk grouping uses PSA, Grade Group/Gleason score, clinical T stage, number/percentage of positive cores, and imaging stage. Genomic classifiers and digital pathology AI are being added to refine prognosis.

Emerging AI models are beginning to answer more clinically useful questions:

- Who is likely to benefit from adding ADT to radiotherapy?
- Who is likely to benefit from longer versus shorter ADT?
- Who is at higher risk of distant metastasis after biochemical recurrence?
- Which post-prostatectomy patients need treatment intensification or closer surveillance?

These are important because they move AI from “diagnosis support” toward **predictive treatment selection**.

### 4. Localized treatment targeting

For focal therapy and focal radiation boost, the key problem is spatial: where exactly is the clinically important cancer, and how much margin is needed?

Tools used or being studied include:

- mpMRI lesion contouring;
- MRI/ultrasound fusion biopsy maps;
- transperineal template mapping;
- PSMA PET/MRI or PET/CT co-registration;
- radiomics-based dominant lesion identification;
- AI segmentation of prostate, lesions, urethra, rectum, bladder, neurovascular bundles;
- dose-painting/focal boost planning;
- 3D focal therapy planning and ablation-margin tools.

**Important distinction:** focal radiation boost is currently better validated than most focal ablative therapy because randomized FLAME data support boosting an MRI-visible dominant lesion during whole-prostate radiotherapy. Most focal ablation approaches still need registry/trial framing and biopsy-based follow-up.

## Current and emerging tool classes

| Tool class | Examples / data inputs | Current role | Validation status |
|---|---|---|---|
| **Clinical nomograms/risk calculators** | PSA, age, DRE, family history, prostate volume, prior biopsy, Grade Group, stage | Biopsy decision, staging, lymph-node risk, recurrence risk, treatment discussions | Widely used; performance depends on population calibration |
| **MRI-enhanced calculators** | PI-RADS, lesion features, prostate volume, PSA density plus clinical variables | Estimate clinically significant cancer risk before biopsy | Increasing validation; may reduce unnecessary biopsies |
| **Biomarker + MRI pathways** | Stockholm3, Proclarix, PHI/4K-like blood tests plus MRI | Improve biopsy triage and reduce low-value biopsies | Some prospective evidence; local availability varies |
| **PSMA PET + MRI calculators** | mpMRI PI-RADS + PRIMARY score/PSMA uptake + PSA/clinical features | Detection of clinically significant cancer before biopsy and staging selected patients | Promising; not universal standard before initial biopsy |
| **AI MRI lesion detection/segmentation** | bpMRI/mpMRI images | Reader support, triage, prostate/lesion contours, biopsy targeting | Many retrospective studies; deployment studies emerging |
| **AI pathology** | Digitized biopsy/prostatectomy slides | Grade support, tumour quantification, prognosis, treatment-benefit modelling | Rapidly developing; some tests entering clinical use/validation |
| **Radiomics / ML treatment planning** | MRI ADC/DWI/DCE, PSMA PET SUV, CT planning images, contours | Dominant lesion mapping, focal boost, biologically targeted radiotherapy | Mostly early/proof-of-concept; needs outcome validation |
| **Multimodal predictive AI** | Pathology images + PSA + Grade Group + T stage + treatment data, sometimes molecular data | Predict metastasis risk or ADT/radiotherapy treatment benefit | Strong retrospective trial-based evidence for some models; prospective implementation still needed |

## Evidence synthesis by use-case

### A. Biopsy decision support

MRI-enhanced risk calculators and biomarker pathways are closest to routine clinical use. The decision is usually not “AI says cancer/no cancer,” but “given PSA, PSA density, MRI, prostate volume, age, DRE, family history, prior biopsy, and biomarkers, is biopsy justified?”

Examples include MRI-enhanced ERSPC-style calculators, PLUM, Mount Sinai prebiopsy calculator, Stockholm3-MRI strategies, Proclarix, and newer models incorporating PSMA PET/CT.

### B. MRI and PSMA PET integration

mpMRI is strong for local lesion detection and staging, but it misses some clinically significant cancers. PSMA PET can identify some MRI-invisible tumours and can improve staging, especially in intermediate/high-risk disease. Combined MRI+PSMA PET pathways are therefore attractive for:

- equivocal MRI;
- PI-RADS 2–3 with persistent clinical concern;
- high-risk staging;
- biopsy targeting;
- defining dominant lesions for focal boost or focal therapy.

However, PSMA PET is not yet a general replacement for MRI or biopsy in initial diagnosis.

### C. AI and radiomics for local treatment targeting

Radiomics and deep learning may help identify dominant intraprostatic lesions and biologically aggressive regions. This matters for:

- focal radiation boost/microboost;
- biologically targeted radiotherapy dose painting;
- focal therapy ablation planning;
- biopsy target prioritization;
- deciding whether disease is too multifocal for focal therapy.

The main limitation is that most studies are retrospective or small, often using prostatectomy whole-mount pathology as a reference. That is useful for training models, but it does not prove that AI-guided treatment improves long-term outcomes.

### D. Digital pathology and multimodal AI for treatment selection

AI pathology is increasingly important because prostate biopsy interpretation drives treatment decisions. AI may reduce variability in cancer detection, Gleason grading, pattern 4 quantification, cribriform/intraductal recognition, tumour volume estimation, and outcome prediction.

The most clinically important emerging class is **predictive** multimodal AI: models trained on randomized trials to identify which patients benefit from treatment intensification, such as adding ADT to radiotherapy or using longer ADT duration in high-risk disease.

**Patient-facing distinction:**

- A **prognostic** model says “your risk is higher or lower.”
- A **predictive** model says “you are more or less likely to benefit from this treatment.”

Predictive models are more directly useful for treatment choice, but they need especially strong validation.

## Selected papers and tools

### Integrated biopsy decision support

#### STHLM3-MRI: risk prediction + MRI + targeted biopsy

- **Citation:** Eklund M, et al. *The Lancet Oncology*. 2021.
- **DOI/PMID:** DOI [10.1016/S1470-2045(21)00348-X](https://doi.org/10.1016/S1470-2045(21)00348-X); PMID [34391509](https://pubmed.ncbi.nlm.nih.gov/34391509/)
- **Evidence type:** Prospective population-based randomized open-label non-inferiority trial.
- **Population:** Men undergoing prostate cancer screening.
- **Patient relevance:** Shows a pathway combining risk prediction, MRI, and targeted biopsy rather than PSA alone.
- **Main finding:** Risk-prediction/MRI/targeted-biopsy strategy can maintain clinically significant cancer detection while reducing unnecessary biopsy and overdiagnosis pathways.
- **Limitations:** Screening setting; local test availability and healthcare system matter.
- **Questions for clinician:** Is a risk-prediction + MRI pathway available before biopsy, and what threshold triggers biopsy?

#### PLUM MRI-based prostate biopsy risk calculator

- **Citation:** *BJU International*. 2023.
- **DOI/PMID:** DOI [10.1111/bju.15835](https://doi.org/10.1111/bju.15835); PMID [35733400](https://pubmed.ncbi.nlm.nih.gov/35733400/)
- **Evidence type:** Development and external validation of mpMRI-based risk calculator.
- **Population:** Men undergoing mpMRI before biopsy.
- **Patient relevance:** Example of integrating PI-RADS/prostate MRI variables with clinical data before biopsy.
- **Main finding:** MRI-inclusive risk calculation improved individualized prediction of clinically significant prostate cancer compared with clinical variables alone.
- **Limitations:** Calculator performance depends on MRI quality, PI-RADS reporting, biopsy technique, and external calibration.
- **Questions for clinician:** Does the calculator apply to my setting: biopsy-naïve, prior negative biopsy, prior low-grade cancer, or negative MRI?

#### Mount Sinai prebiopsy risk calculator

- **Citation:** *European Urology Open Science*. 2022.
- **DOI/PMID:** DOI [10.1016/j.euros.2022.04.017](https://doi.org/10.1016/j.euros.2022.04.017); PMID [35813258](https://pubmed.ncbi.nlm.nih.gov/35813258/)
- **Evidence type:** Development/validation of MRI + clinical risk tool with advanced neural networking validation.
- **Population:** 1902 men undergoing biopsy.
- **Patient relevance:** Illustrates the clinical trend toward web-based individualized risk calculators using MRI and clinical data.
- **Main finding:** MRI and clinical data can be integrated to predict any prostate cancer and clinically significant prostate cancer.
- **Limitations:** Single-system development; online tools need external validation and calibration.
- **Questions for clinician:** Which risk calculator does this clinic use, and is it validated in similar patients?

#### Proclarix blood-based test for biopsy decision-making

- **Citation:** *European Urology Oncology*. 2022.
- **DOI/PMID:** DOI [10.1016/j.euo.2020.12.003](https://doi.org/10.1016/j.euo.2020.12.003); PMID [33422560](https://pubmed.ncbi.nlm.nih.gov/33422560/)
- **Evidence type:** Prospective real-world multicentre study.
- **Population:** Men with PSA 2–10 ng/mL, normal DRE, enlarged prostate, presenting for biopsy.
- **Patient relevance:** Example of blood-based risk scoring used alongside clinical/imaging decision-making.
- **Main finding:** Proclarix risk score helped support biopsy decision-making in a difficult PSA range.
- **Limitations:** Not an imaging AI model; availability varies; should be interpreted with MRI and clinical context.
- **Questions for clinician:** Would an additional blood biomarker meaningfully change my biopsy decision after MRI and PSA density?

### PSMA PET + MRI integration

#### PRIMARY: additive value of PSMA PET/CT to mpMRI triage

- **Citation:** *European Urology*. 2021.
- **DOI/PMID:** DOI [10.1016/j.eururo.2021.08.002](https://doi.org/10.1016/j.eururo.2021.08.002); PMID [34465492](https://pubmed.ncbi.nlm.nih.gov/34465492/)
- **Evidence type:** Prospective multicentre diagnostic study.
- **Population:** Men being evaluated for prostate cancer diagnosis.
- **Patient relevance:** Tests whether PSMA PET/CT adds diagnostic value to mpMRI before biopsy.
- **Main finding:** PSMA PET/CT added diagnostic information to mpMRI triage and informed the PRIMARY score concept.
- **Limitations:** PSMA PET availability/cost/radiation exposure; not yet a universal first-line prebiopsy test.
- **Questions for clinician:** Is PSMA PET being used for staging, biopsy targeting, equivocal MRI, or research?

#### MRI + PSMA PET/CT risk calculator before transperineal biopsy

- **Citation:** *European Urology Open Science*. 2023.
- **DOI/PMID:** DOI [10.1016/j.euros.2023.05.002](https://doi.org/10.1016/j.euros.2023.05.002); PMID [37441340](https://pubmed.ncbi.nlm.nih.gov/37441340/)
- **Evidence type:** Risk calculator development using clinical variables, mpMRI, and PSMA PET/CT.
- **Population:** 291 men from the PRIMARY prospective trial undergoing mpMRI, PSMA PET/CT, and transperineal biopsy.
- **Patient relevance:** Directly matches the question of combining PSA/clinical data, MRI, PSMA PET, and biopsy risk.
- **Main finding:** Models incorporating both mpMRI and PSMA PET/CT parameters were developed to predict overall and clinically significant prostate cancer.
- **Limitations:** Needs external validation; not yet routine standard of care.
- **Questions for clinician:** Would combined MRI+PSMA PET meaningfully change biopsy targeting or treatment planning in my risk group?

#### PRIMARY score for intraprostatic PSMA PET patterns

- **Citation:** *Journal of Nuclear Medicine*. 2022.
- **DOI/PMID:** DOI [10.2967/jnumed.121.263448](https://doi.org/10.2967/jnumed.121.263448); PMID [35301240](https://pubmed.ncbi.nlm.nih.gov/35301240/)
- **Evidence type:** Diagnostic imaging score development.
- **Patient relevance:** Provides a structured way to interpret intraprostatic PSMA PET/CT patterns for diagnosis.
- **Main finding:** PRIMARY score was proposed to optimize prostate cancer diagnosis using intraprostatic PSMA PET/CT patterns.
- **Limitations:** Imaging score, not a stand-alone treatment selector; biopsy confirmation remains central.
- **Questions for clinician:** If PSMA PET shows uptake, how will it be correlated with MRI and biopsy cores?

### AI/radiomics for local treatment targeting

#### PSMA PET + mpMRI radiomics for biologically targeted radiotherapy

- **Citation:** *EJNMMI Research*. 2023.
- **DOI/PMID:** DOI [10.1007/s00259-021-05631-6](https://doi.org/10.1007/s00259-021-05631-6); PMID [37099047](https://pubmed.ncbi.nlm.nih.gov/37099047/)
- **Evidence type:** Imaging/radiomics study co-registering PSMA PET/CT, mpMRI, and histopathology.
- **Population:** 19 prostate cancer patients.
- **Patient relevance:** Addresses targeting information for local radiotherapy planning.
- **Main finding:** Explored voxel-wise relationships and radiomic machine-learning models to predict tumour location and grade using PSMA PET and mpMRI.
- **Limitations:** Small study; research framework; not proof of outcome improvement.
- **Questions for radiation oncologist:** Could MRI and PSMA PET together better define a dominant lesion for focal boost, and how is registration uncertainty handled?

#### Rad-TRaP: radiomics-based targeted radiotherapy planning

- **Citation:** *Radiation Oncology*. 2016.
- **DOI/PMID:** DOI [10.1186/s13014-016-0718-3](https://doi.org/10.1186/s13014-016-0718-3); PMID [27829431](https://pubmed.ncbi.nlm.nih.gov/27829431/)
- **Evidence type:** Computational framework for MRI radiomics, registration, and focal radiotherapy planning.
- **Patient relevance:** Shows how AI/radiomics can be translated into target volumes and dose planning.
- **Main finding:** Proposed a workflow for radiomics-based lesion detection, MRI-to-CT registration, and targeted brachytherapy/EBRT planning.
- **Limitations:** Retrospective proof-of-concept; not clinical outcome validation.
- **Questions for clinician:** Is any proposed boost volume based on validated clinical contours, research radiomics, or both?

#### CorrSigNIA MRI-pathology deep learning framework

- **Citation:** *Medical Image Analysis*. 2022.
- **DOI/PMID:** DOI [10.1016/j.media.2021.102288](https://doi.org/10.1016/j.media.2021.102288); PMID [34784540](https://pubmed.ncbi.nlm.nih.gov/34784540/)
- **Evidence type:** MRI-pathology correlation and deep learning framework.
- **Patient relevance:** Example of using prostatectomy pathology as ground truth to teach AI where aggressive cancer is on MRI.
- **Main finding:** Developed a framework to selectively identify/localize indolent and aggressive prostate cancers on MRI.
- **Limitations:** Research framework; prostatectomy-derived training may not directly translate to all biopsy-era decisions.
- **Questions for clinician:** Is AI being used to support lesion localization, or is it validated to change treatment decisions?

#### Research-based clinical deployment of prostate MRI AI

- **Citation:** *Abdominal Radiology*. 2025.
- **DOI/PMID:** DOI [10.1007/s00261-025-05014-7](https://doi.org/10.1007/s00261-025-05014-7); PMID [40418374](https://pubmed.ncbi.nlm.nih.gov/40418374/)
- **Evidence type:** Prospective clinical workflow/deployment study.
- **Patient relevance:** Shows the implementation problem: an AI model must work inside PACS/radiology workflow, not just in a research notebook.
- **Main finding:** Integrated AI-based prostate/lesion segmentation into clinical PACS under a prospective trial scenario.
- **Limitations:** Workflow deployment is not the same as proving better diagnosis or survival.
- **Questions for clinician:** Is the AI tool used for research, second-reader support, or direct clinical reporting?

### Digital pathology and multimodal AI for treatment decisions

#### AI predictive model for hormone therapy use in prostate cancer

- **Citation:** *NEJM Evidence*. 2023.
- **DOI/PMID:** DOI [10.1056/evidoa2300023](https://doi.org/10.1056/evidoa2300023); PMID [38320143](https://pubmed.ncbi.nlm.nih.gov/38320143/)
- **Evidence type:** AI model developed from pretreatment prostate tissue images and clinical data from phase III randomized trials; validation in RTOG 9408.
- **Population:** Patients treated with radiotherapy with or without short-term ADT.
- **Patient relevance:** Example of predictive AI: identifying who may benefit from adding hormone therapy to radiotherapy.
- **Main finding:** Locked AI model was validated for predicting benefit from ADT in a randomized-trial context.
- **Limitations:** Needs clinical implementation validation; applicability depends on risk group, treatment setting, tissue quality, and model access.
- **Questions for radiation oncologist:** Is any AI biomarker available to estimate whether ADT adds benefit for my risk group, and has it been validated prospectively?

#### AI digital pathology biomarker for long-term vs short-term ADT in high-risk disease

- **Citation:** *Journal of Clinical Oncology*. 2025.
- **DOI/PMID:** DOI [10.1200/JCO.24.00365](https://doi.org/10.1200/JCO.24.00365); PMID [40239134](https://pubmed.ncbi.nlm.nih.gov/40239134/)
- **Evidence type:** Multimodal AI-derived predictive biomarker trained and validated across multiple phase III radiotherapy trials.
- **Population:** Men with high-risk localized prostate cancer receiving radiotherapy plus different ADT durations.
- **Patient relevance:** Directly relevant to treatment-intensity decisions: whether long-term ADT adds benefit over short-term ADT.
- **Main finding:** Developed and validated an AI pathology/clinical biomarker to predict differential benefit from long-term ADT for distant metastasis.
- **Limitations:** Retrospective analysis of trial material; prospective implementation and health-system adoption are still evolving.
- **Questions for clinician:** Could this kind of model eventually guide ADT duration, and is it available/validated in this clinic?

#### Multimodal AI biomarker after prostatectomy biochemical recurrence

- **Citation:** *European Urology*. 2025.
- **DOI/PMID:** DOI [10.1016/j.eururo.2025.12.007](https://doi.org/10.1016/j.eururo.2025.12.007); PMID [41436315](https://pubmed.ncbi.nlm.nih.gov/41436315/)
- **Evidence type:** Digital pathology + clinical-data multimodal AI model validated in NRG/RTOG salvage radiotherapy trials.
- **Population:** Patients with biochemical recurrence after radical prostatectomy receiving salvage therapy.
- **Patient relevance:** Relevant when deciding salvage radiotherapy and hormone therapy after PSA recurrence.
- **Main finding:** Multimodal AI score was associated with distant metastasis risk after salvage therapy.
- **Limitations:** Post-prostatectomy recurrence setting; not a pre-treatment local therapy selector.
- **Questions for clinician:** If PSA recurs after surgery, can pathology/clinical AI refine salvage treatment intensity?

#### AI-based digital histologic classifier for prostate cancer risk stratification

- **Citation:** *JCO Clinical Cancer Informatics*. 2025.
- **DOI/PMID:** DOI [10.1200/CCI.21.00131](https://doi.org/10.1200/CCI.21.00131); PMID [40532127](https://pubmed.ncbi.nlm.nih.gov/40532127/)
- **Evidence type:** Independent blinded validation of digital histology AI prognostic classifier.
- **Population:** Radical prostatectomy cohort with Decipher genomic testing available.
- **Patient relevance:** Shows how AI pathology may complement genomic classifiers for recurrence/metastasis risk.
- **Main finding:** AI-derived pathology scores were associated with biochemical recurrence and distant metastasis risk.
- **Limitations:** Retrospective validation; treatment-decision impact not yet the same as randomized predictive validation.
- **Questions for clinician:** How does AI pathology compare with or add to Decipher/genomic testing and standard pathology?

### Review and implementation papers

#### Next-generation prostate imaging and AI applications

- **Citation:** *Journal of Imaging*. 2025.
- **DOI/PMID:** DOI [10.3390/jimaging11110390](https://doi.org/10.3390/jimaging11110390); PMID [41295107](https://pubmed.ncbi.nlm.nih.gov/41295107/)
- **Evidence type:** Review.
- **Patient relevance:** Broad overview of AI in mpMRI, PSMA PET/CT, TRUS, lesion detection, risk stratification, segmentation, biopsy targeting, and treatment planning.
- **Main finding:** AI may improve accuracy, efficiency, consistency, and treatment planning, but clinical integration, validation, and interpretability remain barriers.
- **Limitations:** Review-level evidence; not a single validated clinical tool.

#### Modern integrative prostate cancer diagnostics

- **Citation:** *Current Opinion in Urology*. 2026.
- **DOI/PMID:** DOI [10.1097/MOU.0000000000001361](https://doi.org/10.1097/MOU.0000000000001361); PMID [41373109](https://pubmed.ncbi.nlm.nih.gov/41373109/)
- **Evidence type:** Review.
- **Patient relevance:** Summarizes radiology AI, pathology AI, and emerging multimodal biomarkers.
- **Main finding:** AI can support radiology/pathology diagnosis and may increasingly integrate multimodal data for prognosis and treatment selection.
- **Limitations:** Many systems are not yet prospectively validated as outcome-improving clinical decision tools.

## Practical clinician discussion checklist

### Before biopsy

- What is my PSA density, not just PSA?
- What is my PI-RADS score and lesion location/size?
- Has my risk been estimated with a calculator that includes MRI?
- Would a blood biomarker such as PHI/4K-like testing, Stockholm3, Proclarix, or another local test change the decision?
- Is PSMA PET being considered because MRI is equivocal, risk is high, or this is a research pathway?

### Before local treatment

- Are MRI findings, biopsy cores, and PSMA PET findings concordant?
- Is the dominant lesion clearly defined for focal therapy or focal boost?
- Is there significant cancer outside the proposed treatment volume?
- Has a targeted plus systematic or template biopsy mapped the gland adequately?
- If AI/radiomics is used to define a target, is it clinically validated or research-only?

### Choosing treatment intensity

- Are decisions based on risk group alone, a nomogram, genomic classifier, AI pathology, or a combination?
- Is the model prognostic or predictive of treatment benefit?
- Does the model estimate benefit from ADT, ADT duration, radiation boost, surgery, salvage therapy, or systemic intensification?
- Has the model been validated in randomized-trial data or only in retrospective cohorts?
- Would the result actually change the recommendation?

### Safety, bias, and validation questions

- Was the AI trained and validated in men similar to me by age, ancestry, PSA range, MRI scanner quality, biopsy method, and disease risk?
- Does the tool perform well in external validation, not just its development centre?
- What false-negative and false-positive rates matter for my decision?
- Who is responsible if AI and clinicians disagree?
- Will the AI result be documented in the medical record and explained in plain language?

## Repository interpretation

This page adds an integrated decision-support layer across the existing PSA, MRI, biopsy, PSMA PET, genomic, focal therapy, and radiotherapy sections. The practical interpretation is:

1. **Risk calculators and nomograms are already mainstream decision support**, even when they are not branded as AI.
2. **MRI-enhanced calculators and biomarker+MRI pathways are closest to routine use before biopsy.**
3. **PSMA PET + MRI integration is promising for biopsy targeting, staging, and dominant-lesion definition**, but not yet a universal replacement for MRI/biopsy pathways.
4. **AI/radiomics for local targeting is promising for focal boost and focal therapy planning**, but most evidence remains retrospective or early clinical deployment.
5. **Digital pathology and multimodal AI are the most promising for treatment-intensity decisions**, especially when validated in randomized trial datasets for ADT or salvage therapy benefit.
6. **The key patient question is not “Is AI being used?” but “Has this tool been externally validated, does it apply to my risk group, and would it change management?”**
