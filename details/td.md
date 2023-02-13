# Detailed Work Items for TD

In addition to the charter, the working group provides overall work items that will be considered for the next charter work.

- **Signing:**
  - Effected Deliverables: Discovery, Thing Description
  - Short Description: Add support for Thing Description signing and support signed Thing Descriptions in the Discovery process. Requires definition of Thing Description canonicalization.
  - Long Description:
- **Timeseries:**
  - Effected Deliverables: Thing Description, Binding Templates
  - Short Description: Add support for describing historical values or value changes of affordances to the TD specification in an interoperable way with existing solutions.
  - Long Description:  Some edge and cloud services can collect property value changes or event emissions for a certain time. This data, called timeseries, can be retrieved by Consumers to display the evolution of the affordance data over time, make predictions about the future values and more. There are different serialization formats and structures of such data in existing solutions. The generic mechanism for timeseries should be introduced in the Thing Description with bindings to existing solutions illustrated in the Binding Templates
    - Related Issues:
      - https://github.com/w3c/wot-thing-description/issues/892

- **Payload Driven Protocols:**
  - Effected Deliverables: Thing Description, Binding Templates, Profiles
  - Short Description: Add support for describing protocols that depend on specific payload structures on top of the protocol bindings. 
  - Long Description:
- **Manageable Actions:**
  - Effected Deliverables: Thing Description, Profiles
  - Short Description: Add support for describing actions that can be managed after their invocation.
  - Long Description:
- **Initial / Common Connection Short Description:**
  - Effected Deliverables: Thing Description, Binding Templates
  - Short Description: Add support for a connection description to be shared among affordance operations
  - Long Description:
- **Canonicalization:**
  - Effected Deliverables: Thing Description, Discovery
  - Short Description: Add a canonicalization algorithm.
  - Long Description:
- **Inline Security:**
  - Effected Deliverables: Thing Description
  - Short Description: Add a way to describe security definitions in a simplified fashion for simple cases.
  - Long Description:
- **TD Versioning:**
  - Effected Deliverables: Thing Description, Discovery
  - Short Description: Explain the semantics on how to version Thing Descriptions.
  - Long Description:
- **Normative TD Parsing, Consuming and Validation:**
  - Effected Deliverables: Thing Description, Scripting API, Profiles
  - Short Description: Define normative algorithms for parsing, consuming and validating Thing Descriptions.
  - Long Description:
- **Linting mechanism for TDs:**
  - Effected Deliverables: Thing Description, Profiles
  - Short Description: Define a linting mechanism for Thing Descriptions that allows adding additional rules.
