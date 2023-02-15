# Special Meetings to Discuss Next WoT Charter (First Set)
* Calendar: https://www.w3.org/events/meetings/504ef715-9e3b-44a7-b8a5-34eab01da99a/20230116T080000
* Dates: Jan 16-18 (CANCELLED)
    - Monday Jan 16: 8am-9am Eastern; logistics [https://lists.w3.org/Archives/Member/member-wot-wg/2022Dec/0007.html Link for Members], [https://lists.w3.org/Archives/Group/group-wot-ie/2022Dec/0007.html Link for IEs]
    - Tuesday Jan 17: 8am-9am Eastern; logistics [https://lists.w3.org/Archives/Member/member-wot-wg/2022Dec/0007.html Link for Members], [https://lists.w3.org/Archives/Group/group-wot-ie/2022Dec/0007.html Link for IEs]
    - Wednesday Jan 18: 8am-10am Eastern; logistics [https://lists.w3.org/Archives/Member/member-wot-wg/2022Dec/0007.html Link for Members], [https://lists.w3.org/Archives/Group/group-wot-ie/2022Dec/0007.html Link for IEs]
    - Thursday Jan 19: 8am-10am Eastern (tentative); logistics [https://lists.w3.org/Archives/Member/member-wot-wg/2022Dec/0007.html Link for Members], [https://lists.w3.org/Archives/Group/group-wot-ie/2022Dec/0007.html Link for IEs]
* Proposals should go here: https://github.com/w3c/wot/tree/main/proposals/deliverable-proposals
* Charter template/starting point: https://github.com/w3c/wot/blob/main/charters/wot-wg-2022-draft.html
* To do: check latest template at https://github.com/w3c/charter-drafts/blob/gh-pages/charter-template.html
* Liaisons: https://github.com/w3c/wot/issues/978#issuecomment-1359830278

## Preparation 
* [https://github.com/w3c/wot/tree/main/proposals/deliverable-proposals Deliverable proposals] have all been merged
* Please make PRs against [https://github.com/w3c/wot/blob/main/charters/wot-wg-2023-draft.html WG 2023 Draft Charter] going forward for proposed deliverables

## Agenda Day 1 - Jan 16 
Length: 1h

Chair: McCool

Scribe: Ege

* Organization (15m)
    - [https://www.w3.org/Guide/process/charter.html W3C Process Guide] [https://www.w3.org/Consortium/Process/Drafts/ (2023 Draft)]
    - [https://github.com/w3c/wot/blob/main/charters/README.md README - WoT Charter Process]
* Starting Point:
    - [https://github.com/w3c/wot/pull/1050 Template] (5m)
* Use Cases and Requirements (30m)
    - Process (15m)
        * (link to Process presentation) 
        * [https://github.com/w3c/wot-usecases/issues/206 Adoption policy - discussion issue]
    - Coverage (15m)
        * https://github.com/w3c/wot-usecases/blob/main/USE-CASES/coverage.csv
        * https://github.com/w3c/wot-usecases/blob/main/USE-CASES/coverage-gaps.md

## Agenda Day 2 - Jan 17 
Length: 1h

Chair: McCool

Scribe: Kaz

* Organization (25m)
    - [https://github.com/w3c/wot/pull/1049 Schedule for remainder of current charter]
    - Charter Extension - how long is really needed? (10m)
    - [https://github.com/w3c/wot/blob/main/PRESENTATIONS/2023-CharterDiscussions/2023-01-17-WoT-Registry-Korkan.pdf Registries - what are they, do we want to use them?] (25m)
* Deliverables (5m)
    - Short review of PRs

Carried forward:
* Security
    - Onboarding process
    - Consolidation of security assertions
    - Key distribution e.g. via DID
* Discovery
    - Geolocation (TD/data vocab + query filters)
    - Normative query language (e.g. JSON Path)
    - Registry for Introductions?
* Architecture update
* TD update
* Profile update
* Scripting

## Agenda Day 3 - Jan 18 
Length: 2h

Chair: Sebastian

Scribe: Michael McCool (first hour), Michael Koster (second hour)

* Organization (10m)
* Generic (5m)
    - Simple fixes: https://github.com/w3c/wot/pull/1058
* Policy and Workflow (40m)
    - Extension (10m) 
        * Extend current charter 4mo or 6mo?
        * Either way, we would plan to start new charter June 1 (or earlier), and proceed with planned high-priority items e.g. OPC UA liaison and TD 2.0.
        * Even if do 6mo extension, should stick to the proposed schedule, which is based on 4mo
    - License (5m)
        * Propose using W3C Software and Document License, as in our current charter
        * PR: https://github.com/w3c/wot/pull/1062
    - Clarify policies (15m)
        * prioritize WoT's actual industry applications working with existing IoT standards like OPC UA and ECHONET Lite Web API
**** Issue (Use cases - Adoption Policy): https://github.com/w3c/wot-usecases/issues/206
        * clarify the relationship between the WoT-WG and related groups/organizations, e.g., WoT IG, WoT CG, WoT-JP CG, DID WG, JSON-LD WG, OPC, ECHONET, ITU-T, Matter, ... (see below for other liaison discussions)
    - Example deliverable template for liaisons:
        * What: Binding Templates, Vocabulary and Ontology, Conformance tests
        * How: A separate joint WG?, WoT WG as a joint WG?, a TF within the WoT WG?, just part of the TD/Binding discussion?
        * Who: Editors from W3C, OPC and/or ECHONET?
        * Resources: [https://github.com/w3c/wot/blob/main/liaisons/opcf/tech_reqs.md Technical Requirements for OPC UA liaison]
        * PR: https://github.com/w3c/wot/pull/1059
    - Decision Policy (10m)
        * See https://w3c.github.io/charter-drafts/charter-template.html#decisions
        * PR: https://github.com/w3c/wot/pull/1061
        * Related to [https://github.com/w3c/wot/pull/1005 Async process proposal]
    - Deliverables - continued (50m)
    - Security
        * Work items: https://github.com/w3c/wot/pull/1053
        * Deliverables: https://github.com/w3c/wot/pull/1057
        * Onboarding process
        * Consolidation of security assertions
        * Key distribution e.g. via DID
    - Discovery
        * Work items: https://github.com/w3c/wot/pull/1052
        * Deliverables: https://github.com/w3c/wot/pull/1060
        * Geolocation (TD/data vocab + query filters)
        * Normative query language (e.g. JSON Path)
        * Filters (also used for geolocation)
        * Registry for Introductions?
    - Architecture update
    - TD update
    - Profile update
        * PR: https://github.com/w3c/wot/pull/1056
    - Scripting
    - Bindings Templates update
        * Registry?

## Agenda Day 4 - Jan 19 
Length: 1h

Chair: McCool

Scribe: Sebastian/Kaz

* Organization (5m)
    - Schedule to finalize
    - "Other" topics: https://github.com/w3c/wot/issues/1051
* Profiles (5m)
    - PR: https://github.com/w3c/wot/pull/1056
* Liaisons (25m)
    - PR: https://github.com/w3c/wot/pull/1059
    - Related Internal W3C Groups
        * DID
        * JSON-LD
        * ?
    - Bindings and registries
        * OPC-UA
        * BACNET
        * ECHONET
        * CSA/Matter
    - Digital Twins
        * https://github.com/w3c/wot/issues/978#issuecomment-1359830278
        * DTDL
        * AAS
* Thing Description
    - PR: https://github.com/w3c/wot/pull/1063
