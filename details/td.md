# Detailed Work Items for TD

In addition to the charter, the working group provides overall work items that will be considered for the next charter work.

- **Signing:**
  - Effected Deliverables: Discovery, Thing Description
  - Short Description: Add support for Thing Description signing and support signed Thing Descriptions in the Discovery process. Requires definition of Thing Description canonicalization.
  - Long Description: Mechanisms for signing TDs documents were under discussion in the last charter but were not mature enough to include. Adding support for TD canonicalization and signing would be helpful to ensure that TDs are not intercepted and modified by third parties. Verifying a signature requires identity management, i.e. the verifier needs to know or have trusted access to the public key of the signer. Directories need to be extended to verify signatures and generate new chained signatures as needed. 
- **Timeseries:**
  - Effected Deliverables: Thing Description, Binding Templates
  - Short Description: Add support for describing historical values or value changes of affordances to the TD specification in an interoperable way with existing solutions.
  - Long Description:  Some edge and cloud services can collect property value changes or event emissions for a certain time. This data, called timeseries, can be retrieved by Consumers to display the evolution of the affordance data over time, make predictions about the future values and more. There are different serialization formats and structures of such data in existing solutions. The generic mechanism for timeseries should be introduced in the Thing Description with bindings to existing solutions illustrated in the Binding Templates
    - Related Issues:
      - https://github.com/w3c/wot-thing-description/issues/892

- **Payload Driven Protocols:**
  - Effected Deliverables: Thing Description, Binding Templates, Profiles
  - Short Description: Add support for describing protocols that depend on specific payload structures on top of the protocol bindings. 
  - Long Description:  Some protocols are built on top of the application layer protocols. Some examples are:

    - RPC protocols on top of HTTP such as JSON-RPC.
    - Protocols using MQTT topics together with payloads to identify affordances.
    - Websocket sub-protocols.
    - SSE usage across implementations.
    - Webhook usage across implementations.

    The Thing Description should be updated with mechanisms that make it possible to describe such protocols while optimizing the TD instances to be human and machine readable. The Binding Templates should be updated with concrete cases where this mechanism is already used. The Profiles can use this mechanism to reduce the size of TDs while making them easier to understand. The working group will also document in which cases this method does not work due to making the TDs too complicated to understand, thus requiring a binding document. 
- **Manageable Actions:**
  - Effected Deliverables: Thing Description, Profiles
  - Short Description: Add support for describing actions that can be managed after their invocation.
  - Long Description:  Various use cases require the implementation of more complex actions that span multiple protocol transactions. Such actions are not simply invoked but need to managed over time by the Thing and the Consumer. These are covered in the WoT Thing Description 1.1 via the initiation (invokeaction), monitoring (queryaction), and cancellation (cancelaction) of ongoing actions. However, the following points are not supported:

    - Sent and received payloads associated to the operations
    - Management of dynamically generated identifiers
    - Describing queues of actions

    These limitations are also influencing the Profiles specification.

    Additionally, there have been proposals by the WG members that need to taken into account and evaluated:

    - https://github.com/w3c/wot-thing-description/tree/main/proposals/hypermedia-control
    - https://github.com/w3c/wot-thing-description/tree/main/proposals/hypermedia-control-2
    - https://github.com/w3c/wot-thing-description/tree/main/proposals/hypermedia-control-3

    Related Issues:

    - https://github.com/w3c/wot-thing-description#1692
    - https://github.com/w3c/wot-thing-description#1644
    - https://github.com/w3c/wot-thing-description#1223

- **Initial / Common Connection Short Description:**
  - Effected Deliverables: Thing Description, Binding Templates
  - Short Description: Add support for a connection description to be shared among affordance operations
  - Long Description:  Currently, each form of an affordance has information on the endpoint, media type and other protocol related information. It is possible to use the base term for simplifying the endpoint but it has limitations such as:

    - If the media type is also common across forms, it is repeated
    - Multiple bases are not possible
    - For protocols that are based on an initial connection and then subsequent messages, the semantics are not clear.

    Thus, a mechanism to describe connection and protocol information that can be used by other forms is needed. In protocols with initial connection, this can be also used to indicate what needs to be done by the Consumer before executing any operation.

    Related Issues:

    - https://github.com/w3c/wot-thing-description/issues/1664
    - https://github.com/w3c/wot-thing-description/issues/1248
    - https://github.com/w3c/wot-thing-description/issues/1242
    - https://github.com/w3c/wot-thing-description/issues/878

- **Canonicalization:**
  - Effected Deliverables: Thing Description, Discovery
  - Short Description: Add a canonicalization algorithm.
  - Long Description:  Thing Descriptions can contain the same information but serialized differently even in the same serialization format, due to structures such as maps which do not impose an order. This is problematic for comparing TDs or more importantly, for signing them where every byte difference results in a different signature. Thus, the WG will develop a canonicalization algorithm based on JSON-LD.

    Related Issues:

    - https://github.com/w3c/wot-thing-description/issues/1023
    - https://github.com/w3c/wot-thing-description/issues/940

    Some work has been done in the previous charter but has been postponed due to lack of features in JSON-LD. Related PRs:

    - https://github.com/w3c/wot-thing-description/pull/1304
    - https://github.com/w3c/wot-thing-description/pull/1151
    - https://github.com/w3c/wot-thing-description/pull/943
    - https://github.com/w3c/wot-thing-description/pull/1086


- **Inline Security:**
  - Effected Deliverables: Thing Description
  - Short Description: Add a way to describe security definitions in a simplified fashion for simple cases.
  - Long Description:  In order simplify how security mechanisms are described in simple cases, the WG will propose a way to use them with combining the definition and usage into a single term.

    Related Issues:

    - https://github.com/w3c/wot-thing-description/issues/1572
    - https://github.com/w3c/wot-thing-description/issues/757
    - https://github.com/w3c/wot-thing-description/issues/300

    Some work has been done in the previous charter but has been postponed due to backwards compatibility requirement. Related PRs:

    - https://github.com/w3c/wot-thing-description/pull/945

- **TD Versioning:**
  - Effected Deliverables: Thing Description, Discovery
  - Short Description: Explain the semantics on how to version Thing Descriptions.
  - Long Description:  TD allows themselves to be versioned. However, the semantics of such versioning is not defined, i.e. the meaning of version numbers. This makes it difficult to manage TDs and results in different behavior across versioned TD repositories. The WG will define the semantics of versions of a TD and recommendations on how to manage different versions of TDs.

    Related Issues:

    - https://github.com/w3c/wot-thing-description/issues/257
    - https://github.com/w3c/wot-discovery/issues/257

- **Normative TD Parsing, Consuming and Validation:**
  - Effected Deliverables: Thing Description, Scripting API, Profiles
  - Short Description: Define normative algorithms for parsing, consuming and validating Thing Descriptions.
  - Long Description: Currently the TD specification defines an abstract information model and a default JSON serialization for TDs. However, parsing, consuming and validating TDs are not normatively defined. A validation process is defined but is not normative, which leads to certain ambiguities for a Consumer parsing a TD. Additionally, no method is proposed for validation the extensions that are used via the prefixes and the @context. The WG will specify normative algorithms for parsing, consuming and validating TDs to ensure interoperability of Consumers. 
- **Linting mechanism for TDs:**
  - Effected Deliverables: Thing Description, Profiles
  - Short Description: Define a linting mechanism for Thing Descriptions that allows adding additional rules.
  - Long Description:  Linting rules exist for programming languages or for API specifications in order to establish custom rules within projects. How these rules can be defined for TDs is not specified in any way, making it difficult to constrain flexibility of TDs in a standardized manner. The WG will define the mechanism for linting TDs together with optional rules that can be used by different projects.

    Related Issues:

    - https://github.com/w3c/wot-thing-description/issues/1707
    - https://github.com/w3c/wot-thing-description/issues/1512
    - https://github.com/w3c/wot-thing-description/issues/1195

