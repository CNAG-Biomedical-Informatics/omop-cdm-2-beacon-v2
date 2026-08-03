# Enhancing semantic interoperability in precision medicine: converting OMOP CDM to Beacon v2 in the Spanish IMPaCT-Data project

This is the companion repository for our [BMC Medical Informatics and Decision Making article](https://doi.org/10.1186/s12911-026-03649-0). It provides a tutorial for the paper's file-based workflow: converting OMOP CDM 5.4 SQL exports or CSV tables into JSON for the `individuals` entity of the [GA4GH Beacon v2 Models](https://docs.genomebeacons.org/schemas-md/individuals_defaultSchema).

The paper also describes an on-the-fly architecture that connects a PostgreSQL OMOP CDM database directly to a Beacon v2 API. That architecture is outside the scope of this tutorial.

## Tutorial

The notebook uses synthetic [EUNOMIA](https://ohdsi.github.io/Eunomia/) data and covers:

- installation of the tested Convert-Pheno 0.34 release;
- SQL-dump conversion and export of parsed OMOP tables as CSV;
- standard and memory-efficient streaming conversion;
- selection of specific OMOP CDM tables; and
- calculation of conversion-completeness statistics.

Run the interactive version in Google Colab:

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1mRsR9FRVhp8FTu6nW0IRBUiGxFSNaUmA)

The version tracked in this repository is [nb/omop_cdm_2_beacon_v2_tutorial.ipynb](nb/omop_cdm_2_beacon_v2_tutorial.ipynb).

The notebook is designed for a Linux-based Google Colab runtime: it uses `/content`, `apt-get`, and `google.colab`. To use it in a local Jupyter environment, adapt those Colab-specific paths and cells. Generated files are written to `/content` and are removed when the Colab runtime is recycled.

> [!CAUTION]
> The tutorial data are synthetic. Do not upload confidential, personal, or patient-identifiable data to a managed Colab runtime unless that use has been approved by your institution and complies with the applicable governance and data-protection requirements. Use an appropriately controlled environment for sensitive data.

## Convert-Pheno

Convert-Pheno performs the file-based transformation demonstrated in the notebook:

- [Source code](https://github.com/CNAG-Biomedical-Informatics/convert-pheno)
- [Documentation](https://cnag-biomedical-informatics.github.io/convert-pheno/)
- [CPAN distribution](https://metacpan.org/pod/Convert::Pheno)
- [Docker images](https://hub.docker.com/r/manuelrueda/convert-pheno/tags)

## Citation

If you use this tutorial in your work, please cite:

> Rueda M, Ramírez-Anguita JM, López-Sánchez V, et al. Enhancing semantic interoperability in precision medicine: converting OMOP CDM to Beacon v2 in the Spanish IMPaCT-Data project. BMC Medical Informatics and Decision Making. 2026.

<https://doi.org/10.1186/s12911-026-03649-0>
