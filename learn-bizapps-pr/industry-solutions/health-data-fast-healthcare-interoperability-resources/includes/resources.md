A FHIR resource is a discrete piece of data representing an entity in a real-world healthcare interaction. Entities such as a patient, a practitioner, a procedure, a medication, and so on, are all represented as resources in FHIR. FHIR resources structure information as it is generated in real-world healthcare settings.

> [!div class="mx-imgBorder"]
> ![A diagram to show the relationship between resources and U R Ls.](../media/urls.png)

**All** FHIR resource types have:

- A "canonical URL" where the structure of the resource type is defined (for example, `http://hl7.org/fhir/StructureDefinition/Patient`)

- Four data elements - ID, metadata, implicitRules, and language

- Elements within metadata including versionId, lastUpdated, source, profile, security, tag

- An extensibility framework to support evolving methods in healthcare

The common resource types (such as Patient, Practitioner, Encounter, Observation, etc.) have a set of defined data elements specific to the real-world domain of the resource (such as the gender element for the Patient resource), different for each resource type.

FHIR resource instances (on a FHIR server) have a unique, server-wide resource ID (like "123") with a resource instance URL (for example, `{{fhirurl}}/Patient/123`).

Resources can generally be classified in the context of the following five categories:

> [!div class="mx-imgBorder"]
> ![Diagram showing resources surrounded by the following categories.](../media/categories.png)

**Types** - categories as defined by HL7 that help to distinguish the function of resources including

- Clinical

- Financial

- Specialized

**Elements** - attributes that distinguish every resource instance

- **id** - the server-wide resource ID unique to each resource instance on a FHIR server

- **metadata** - for storing information like the profile on which the resource is based

- **implicitRules** - for indicating special restrictions on a resource instance

- **language** - the human language used to record information (English, Spanish, etc.)

- the domain-specific elements for the common resources (such as the gender element for the Patient resource, etc.)

**Structure** - for defining the schema of each resource type, including its data types, extensions, and constraints

- **Narratives** - XHTML-formatted information about a resource for display in a user interface

- **Extensions** - a framework for adding new structure and/or elements to extend a resource definition

- **Contained resources** - a framework for storing a resource's data within an enclosing resource

**Hierarchy** - for establishing how resources inherit their attributes from the foundational "base" resource class in FHIR

- **DomainResource class** - inherits from the "base" resource class, parent to the common resource types such as Patient, Practitioner, etc.

- **Bundle, Binary, Parameters** - the three resource types in FHIR that inherit directly from the foundational "base" resource class

**Identity** - how and where resource instances are tracked and located

- **Location URL** - for example, `{{fhirurl}}/Patient/123`

- **Location identifiers** - codes used in addition to the resource ID for identifying a resource instance

## Example - Patient resource

Let's take a high-level look at a patient resource. Patient is a normalized resource within the HL7 FHIR specification, meaning that it's universally received and standardized all over the world. There's a set of definitive data elements that are associated with a patient. There will be a unique URL associated with each patient resource instance. That URL can be used by a FHIR client to interact with the patient resource managed by its hosting FHIR server.

FHIR resources contain data items as described by the definition of the resource type. The patient resource includes demographics and other administrative information about an individual receiving health-related service. The US Core Implementation Guide (IG) defines how to implement FHIR in the US. The IG required data elements for a Patient resource define the standard Patient resource structure. A patient resource must include elements that store the patient name, an identifier (such as MRN or SSN) and the patient's gender.

The following is an example of part of a patient resource. You can view the full example [here](https://www.hl7.org/fhir/patient-example.json.html?azure-portal=true).

> [!div class="mx-imgBorder"]
> [![Screenshot of an example of the text of a resource type patient.](../media/patient-resource.png)](../media/patient-resource.png#lightbox)

## Connections between resources in FHIR

The graphic below is just one example of some of the various resources that might be utilized for an event like a patient procedure. The resources shown - Patient, DiagnosticReport, Condition, Procedure, Encounter, Practitioner - are all connected with each other through the subject, report, performer, encounter, and related elements stored in the Procedure resource. These elements in the Procedure resource hold *references* to the other resources. This serves to illustrate how the references between resources form a web of health information in FHIR. While not shown here, other resources could also be referenced, including for administrative functions in the financials category when it comes to billing (for example, the Invoice, Claim and ClaimResponse resources).

> [!div class="mx-imgBorder"]
> ![Diagram to show how resources can interact with one another and include references to other resources.](../media/procedure-resources.png)

Resources are often bundled together when retrieved in a FHIR search. For example, a patient could have an annual physical (Encounter) with their physician (Practitioner) on August 1, 2021. The physician reviewed their family history (FamilyMemberHistory) and decided to order a mammogram (Procedure). When someone conducts a search for information about that particular encounter, all of these resources could be returned within a Bundle resource, with references between the different resources.

> [!div class="mx-imgBorder"]
> ![Diagram to illustrate various resource types.](../media/resource-types.png)
