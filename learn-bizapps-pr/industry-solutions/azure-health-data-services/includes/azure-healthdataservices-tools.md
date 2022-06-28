Azure Health Data Services consists of tools and connectors for protected health information to enable health and life sciences systems interoperability within and across organizations. The following is a high-level look at its key components.

:::image type="content" source="../media/ahds-tools-connectors.png" alt-text="pictures of a database, IoT device, medical image, biomedical image connection to the box that contains Azure workspace." lightbox="../media/ahds-tools-connectors.png":::

## Understanding Azure Health Data Services workspace

The Azure Health Data Services workspace is a logical container for healthcare service instances such as Fast Healthcare Interoperability Resources (FHIR®) services, Digital Imaging and Communications in Medicine (DICOM®) services, and MedTech service.

Key workspace concepts: 

- The workspace creates a compliance boundary (HIPAA, HITRUST) within which protected health information can travel.
- You can provision multiple services within a workspace, and they work more seamlessly with one another.
- Workspaces can be created in a resource group from the Azure portal or using deployment scripts.
- Workspaces provide a single compliance boundary for authentication and authorization of users.
- Role-based access control (RBAC) enables you to manage how your data is stored and accessed.
- Data is isolated to a unique database per API instance and protected with multi-region failover.

The following diagram illustrates how Azure Health Data Services might be provisioned in an Azure subscription:

:::image type="content" source="../media/azure-resource-group.png" alt-text="pictures of a group of rectangular boxes showing the resources namely DICOM, MedTech Service, FHIR and standard configuration settings." lightbox="../media/azure-resource-group.png":::

## FHIR Service
FHIR service in Azure Health Data Services enables rapid exchange of data through FHIR APIs, backed by a managed Platform-as-a Service (PaaS) offering in the cloud with the ability to leverage all of the resources on the Microsoft stack. 
Azure Health Data Services builds on the features and functionality of Microsoft’s original GA solution for FHIR (Azure API for FHIR), with additional capabilities. This includes transaction support for FHIR bundles and high-throughput bulk import of FHIR data into the FHIR service.

Key FHIR service concepts:

- The FHIR API and compliant data store enable you to securely connect and interact with any system that utilizes FHIR APIs.
- Transforming your data to FHIR allows you to connect existing data sources such as the electronic health record systems or research databases.
- FHIR service allows for the exchange of data via consistent, RESTful, FHIR APIs based on the HL7 FHIR specification.

Data is sent or retrieved from one server to another using HTTP requests via the FHIR RESTful API.

:::image type="content" source="../media/azure-fhir-restapi.png" alt-text="pictures of an arrow and post, get, put, patch and delete syntax for the RESTAPI." lightbox="../media/azure-fhir-restapi.png":::

## DICOM Service
DICOM (Digital Imaging and Communications in Medicine) is the international standard to transmit, store, retrieve, print, process, and display medical imaging information, and is the primary medical imaging standard accepted across healthcare.  For example, DICOM helps enable digitization of Ultrasound, CT scan, MRI and other common imaging procedures.

The following diagram illustrates how DICOM might be used to transfer DICOM objects between entities, such as hospitals, to payors as well as other medical centers for second opinions or continued care.  
 
:::image type="content" source="../media/dicom-objects.png" alt-text="Picture of a hospital, insurance company, medical center and how they interact." lightbox="../media/dicom-objects.png":::

The DICOM data model consists of four object levels Patient, Study, Series & Equipment and Instance (image).

:::image type="content" source="../media/dicom-data-model.png" alt-text="Picture consists of rectangles and arrows showing the four object levels Patient, Study, Series & Equipment." lightbox="../media/dicom-data-model.png":::

The DICOM service is a managed service within Azure Health Data Services that ingests and persists DICOM objects at multiple thousands of images per second.

Key DICOM service concepts:

- Facilitate communication and transmission of imaging data with any DICOMweb™ enabled systems or applications via DICOMweb standard APIs.
- Isolate data to a unique database per API instance and protected with multi-region failover.
- Index DICOM studies, series, and instances on both standard and private DICOM tags by expanding the list of tags that are already specified within DICOM Conformance Statement.
- Access ordered, guaranteed, immutable, read-only logs of all the changes that occur in DICOM service.
- Inject DICOM metadata into a FHIR service, or FHIR server, as an imaging study resource allowing a single source of truth for both clinical data and imaging metadata.


## MedTech Service
The MedTech service can be used to ingest, and transform to FHIR, high-frequency data from IoT medical devices for monitoring, storage, analysis, and reporting of vital health information.

:::image type="content" source="../media/medtech-service.png" alt-text="pictures of a hospital, ambulance, lab, house with information collection from them and sending it to the MedTech service." lightbox="../media/medtech-service.png":::

Key MedTech service concepts:
- Health data from disparate devices can be aligned and standardized into a common format to make sense of the data through a unified lens and capture trends.
- IoT data is normalized and grouped by mapping commonalities to FHIR.
- Devices and health care consumers can be linked for enhanced insights and trend capture.
- MedTech service may be used with devices created and managed through Azure IoT Hub for enhanced workflows and ease of use.

## Deploying Azure Health Data Services
Azure Health Data Services can be configured using either the Azure Portal or programmatically using Bicep.  

:::image type="content" source="../media/ahds-deploy.png" alt-text="Picture of the UI page for creating a resource with the Overview tab open." lightbox="../media/ahds-deploy.png":::

As part of creating the Azure Health Data Services resource you can provide details to stand up a workspace.

:::image type="content" source="../media/ahds-create-workspace.png" alt-text="Picture of the UI page for creating a workspace with the Basic tab open." lightbox="../media/ahds-create-workspace.png":::

Here you will select your Azure Subscription, the Resource Group where you want to deploy the Azure Health Data Services workspace, and the Azure region where you are located. Also, you will need to supply a name for your workspace.

Once the workspace is created you can deploy the individual services into the workspace. Each service has its own configuration that would need to be completed. 

With Azure Health Data Services you pay only for what you use with consumption-based pricing. Auto scale ensures the service meets the varying demands of your workload.
