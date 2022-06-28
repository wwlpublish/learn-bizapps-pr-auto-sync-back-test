Non-standardized data creates critical problems.  Coordinated care, patient monitoring, alerts, and flexible care options are among the many healthcare functions that rely upon interoperability.

Below are some of the most common challenges to interoperability that Azure Health Data Services helps address:

- **Health data is siloed.** Care and innovation are stifled without an ability to cross-reference or merge coincident data from different sources.
- **Health data structures are non-uniform.** Translating non-uniform health data into a standard format can be labor intensive and error prone. This is a material barrier to AI/ML and analytics workloads.
- **De-identification of non-uniform data is difficult and time consuming.** De-identification of data is often required by law.
- **Geographically unique** datasets are difficult to transform for research (i.e. population health data).
   
## Solving interoperability challenges
Azure Health Data Services is an Azure PaaS service  that enables organizations to bring health data to the Microsoft cloud. Azure Health Data Services enables ingesting, converting and deidentifying protected health information (PHI) to enable health data interoperability within and across organizations.

The service focuses on several internationally adopted data standards, including FHIR and DICOM. [FHIR](https://www.hl7.org/fhir/index.html) is a standard for healthcare data exchange, published by HL7®. FHIR enables a robust, extensible data model with standardized semantics and data exchange that allows all systems using FHIR to work together. Transforming data to FHIR allows users to quickly connect together existing data sources such as electronic health record systems or research databases. SMART on FHIR, which is an extension of the base FHIR standard, enables the rapid exchange of data in modern implementations of mobile and web development. By leveraging the SMART on FHIR standard, app developers can better leverage harmonized health datasets and exchange those datasets between systems. Additionally, FHIR can simplify data ingestion and accelerate development with analytics and machine learning tools.

FHIR provides an alternative to document-centric approaches by directly exposing discrete data elements as resources. For example, basic elements within health records  like patients, admissions, diagnostic reports and medications can each be retrieved and manipulated via their own resource URLs. 

A FHIR resource is a discrete data concept such as a patient, document, medication, family history, health procedure, list of allergies etc.

:::image type="content" source="../media/fhir-data-sources.png" alt-text="Picture of a patient, document, medication, family history, health procedure, list of allergies pushed to the cloud - These are sources of FHIR content " lightbox="../media/fhir-data-sources.png":::

Currently, HL7 designates 145 types of resources.  A FHIR resource is a piece of data you can collect across the internet because it has a physical location that can be located via a URL address submitted in a browser. This, combined with canonized terms and extensions of those terms, makes FHIR a key aspect of improving interoperability.

While FHIR as a standard enables interoperability for better patient outcomes, it is not a replacement IT system for payors, providers, research or pharmaceutical organizations. FHIR will not replace electronic health record (EHR) systems or provider billing systems. FHIR enables the data that needs to be exchanged by these systems by calling FHIR service.

Azure Health Data Services and FHIR enable data interoperability in the following key areas:

- **Health data in a centralized repository**: Azure Health Data Services enables organizations to store and organize their data in a centralized location.
- **Create data uniformity**: Normalized data is universally readable across the HLS sector.
- **Securely de-identified data** can be leveraged for research, clinical, and operational insights.
- **Azure Health Data Services is the “babelfish”** in the cloud, translating data structures into globally recognized formats.

:::image type="content" source="../media/api-azure-healthdata-service.png" alt-text="Picture shows two wheels and the how dat is used in azure data services" lightbox="../media/api-azure-healthdata-service.png"::: 

## Healthcare data connectors
Once processed, health data can be used in reporting and analytics for Power BI data visualizations, Teams notifications, SMART on FHIR user-facing apps, and more.  Additionally, the de-identified data can be used to train models in Azure Machine Learning for identifying patterns and outliers to aid practitioners in making decisions.  

## PHI ready
Protected Health Information (PHI) is regulated with protections that allow for the secure transfer of information as needed to provide care.  This information is personal and includes data such as vitals, diagnosis, care plans, etc. 