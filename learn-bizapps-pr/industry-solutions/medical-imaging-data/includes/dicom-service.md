DICOM service within Azure Health Data Services enables imaging data to securely persist in the Microsoft cloud. DICOM service is a managed Azure service that allows standards-based communication with any DICOMweb™ enabled systems.

> [!div class="mx-imgBorder"]
> [![Diagram of P a a S Service showing health data going into Azure Health Data Services and then out into other systems.](../media/service.png)](../media/service.png#lightbox)

The service ingests and persists DICOM objects from vendor neutral archives (VNA), picture archiving and communications system (PACS), and other medical imaging systems, at multiple thousands of images per second. Azure Health Data Services DICOM service enables you to store DICOM images in the cloud, where you can query, retrieve, and share medical images with ease.

## Medical Imaging Server for DICOM

An open-source version is also available: [Medical Imaging Server for DICOM](https://github.com/microsoft/dicom-server/?azure-portal=true).

## DICOMcast

DICOMcast allows the synchronization of data from DICOM service to a FHIR service, which enables healthcare organizations to merge clinical and imaging data together into a unified database. DICOMcast opens new clinical and research possibilities by integrating textual-based health data with medical imaging data. 

DICOMcast is the first cloud technology to bring DICOM metadata and healthcare data together in FHIR. The technology works by enabling communication across clinical and imaging datasets. For example, for a given patient, DICOMcast makes it possible for providers to view the patient’s FHIR records and medical images together as if they're from the same data store. DICOMcast also enables new interoperability in medical studies, such as radiological queries, by using labeled attributes combined with patients’ health histories in FHIR. 

> [!div class="mx-imgBorder"]
> ![Diagram of the architecture of DICOMcast.](../media/dicom-cast.png)

### DICOMcast operation

The following steps and diagram highlight the DICOMcast operation:

1. **Poll for batch of changes** - DICOMcast polls for changes through the [Change Feed](/azure/healthcare-apis/dicom/dicom-change-feed-overview/?azure-portal=true), which captures changes that occur in your Medical Imaging Server for DICOM.

1. **Fetch corresponding FHIR resources, if any** - If DICOM service changes correspond with FHIR resources, DICOMcast will fetch the related FHIR resources. DICOMcast synchronizes DICOM tags to the FHIR resource types of **Patient** and **ImagingStudy**.

1. **Merge FHIR resources and 'PUT' as a bundle in a transaction** - The FHIR resources that correspond with the DICOMcast captured changes will be merged. The FHIR resources will be 'PUT' as a bundle in a transaction into your FHIR service.

1. **Persist state and process next batch** - DICOMcast will persist the current state to prepare for the next batch of changes.

    > [!div class="mx-imgBorder"]
    > [![Diagram of architecture of DICOMcast, showing DICOM service and F H I R service.](../media/connect.png)](../media/connect.png#lightbox)

## DICOM service features

DICOM service includes the following features:

- **PHI compliant** - Protect your PHI with unparalleled security intelligence. Your data is isolated to a unique database for each API instance and is protected with multi-region failover. DICOM service implements a layered, in-depth defense and advanced threat protection for your data.

- **Extended query tags** - You can index DICOM studies, series, and instances on standard and private DICOM tags by expanding the list of tags that are already specified within the [DICOM Conformance Statement](/azure/healthcare-apis/dicom/dicom-services-conformance-statement/?azure-portal=true).

- **Change feed** - Access ordered, guaranteed, immutable, read-only logs of all changes that occur in DICOM service. Client applications can read these logs anytime, independently, in parallel, and at their own pace.

- **DICOMcast** - Through DICOMcast, DICOM service can inject DICOM metadata into a FHIR service, or FHIR server, as an imaging study resource. This feature allows for a single source of truth for clinical data and imaging metadata, and it's available on demand. To enable DICOMcast for your Azure subscription, make sure that you request access for DICOMcast by opening an [Azure technical support](https://azure.microsoft.com/support/create-ticket/?azure-portal=true) ticket.

- **Region availability** - DICOM service has a wide range of [availability across many regions](https://azure.microsoft.com/global-infrastructure/services/?azure-portal=true&products=health-data-services&regions=all) with multi-region failover protection.

- **Scalability** - DICOM service is designed as an out-of-the-box service that supports different workload levels at a hospital, region, country, and global scale, without sacrificing performance specifications by using autoscaling features.

- **Role-based access** - You control your data. Role-based access control (RBAC) enables you to manage how your data is stored and accessed. By providing increased security and reducing administrative workload, you can determine who has access to the datasets that you create, based on role definitions that you've created for your environment.

## Connect DICOM service with other tools, services, and products

You can connect DICOM service with other tools, services, and products:

- **DICOM data anonymization** [Anonymize DICOM metadata](https://github.com/microsoft/Tools-for-Health-Data-Anonymization/blob/master/docs/DICOM-anonymization.md/?azure-portal=true) - A DICOM file contains a viewable image and a header with a large variety of data elements. These metadata elements include identifiable information about the patient, the study, and the institution. Sharing such sensitive data demands proper protection to ensure data safety and maintain patient privacy. DICOM Anonymization tool helps anonymize metadata in DICOM files for this purpose.

- **Access imaging study resources on Microsoft Power BI, Microsoft Power Apps, and Microsoft Dynamics 365 Customer Insights** - [Connect to a FHIR service from Power Query Desktop](/power-query/connectors/fhir/fhir/?azure-portal=true). After provisioning a DICOM service and a FHIR service, and after synchronizing an imaging study for a given patient through DICOMcast, you can use the Power Query connector for FHIR to import and shape data from the FHIR server, including imaging study resource.

- **Convert imaging study data to hierarchical parquet files** [FHIR to Synapse Sync Agent](https://github.com/microsoft/FHIR-Analytics-Pipelines/blob/main/FhirToDataLake/docs/Deployment.md/?azure-portal=true) - After you provision a DICOM service and a FHIR service, and after you've synchronized an imaging study for a given patient through DICOMcast, you can use FHIR to Synapse Sync Agent to perform analytics and machine learning on imaging study data. Use it by moving FHIR data to Microsoft Azure Data Lake Storage in near real time and making it available to a Microsoft Azure Synapse workspace.
