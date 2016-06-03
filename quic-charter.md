Name: Quick UDP-based Internet Connection (QUIC)

Acronym: QUIC

Area: TSV

Personnel

 * Chairs: TBD
 * Area Director: Spencer Dawkins
 * Security Area Advisor: TBD

# Charter for Working Group

There is emerging implementation and deployment experience with QUIC, a UDP-based protocol that provides a stream-multiplexing encrypted transport. Based on that implementation and deployment experience, the QUIC working group will provide a standards track specification generalizing the design described in the initial set of draft-tsvwg-quic-protocol, draft-tsvwg-quic-loss-recovery, and related documents. 

Key goals for QUIC are: 
 * Minimizing connection establishment and overall transport latency for applications, starting with HTTP/2; 
 * Providing multiplexing without head-of-line blocking; 
 * Enabling deployment over unmodified Internet paths; and 
 * Enabling multipath and forward error correction extensions.

The work of the group will have four main focus areas, corresponding to four core deliverables. 

The first of these is the core transport work, which will describe the wire format, along with the mechanisms for connection establishment, stream multiplexing, data reliability, loss detection and recovery, congestion control, version negotiation, and options negotiation. Work on congestion control will describe use of an existing congestion controller as a default scheme for QUIC. QUIC is expected to support rapid iterability and experimentation, and this work will describe a versioning process that enables distributed experimentation with QUIC. 

The second of these focus areas is security. This work will describe how the protocol uses the facilities of TLS 1.3 for key negotiation and will also describe how those keys are used to provide confidentiality and integrity protection of both application data and QUIC headers. This work will ensure that QUIC using TLS1.3 has security and privacy properties that are at least as good as a stack composed of TLS1.3 using TCP (or MPTCP when using multipath).

The third focus area will describe mappings between specific applications’ semantics and the transport facilities of QUIC. The first mapping will be a description of HTTP/2 semantics using QUIC, specifically with the goal of minimizing web latency using QUIC. This mapping will accommodate the extension mechanisms defined in the HTTP/2 specification. Upon completion of that mapping, additional protocols may be added by updating this charter to include them.

The fourth focus area will extend core protocol facilities to enable multipath capabilities for both connection migration and load sharing.

After the completion of the core protocol deliverable, the group will consider a recharter to complete extensions that will support partial reliability and enable the negotiation and use of FEC schemes. Where possible, the design of the core protocol should not preclude future extensions in this direction. Development of new FEC schemes will not be considered by this group.

Note that consensus is required both for changes to the current protocol mechanisms and retention of current mechanisms. In particular, because something is in the initial document set does not imply that there is consensus around the feature or around how it is specified.

The following work items are explicitly out of scope for this group:
* Defining new congestion control schemes.
* Defining new forward error correction schemes.

## Milestones

* Chartering + 3 Months: Working group adoption of Core Protocol document
* Chartering + 3 Months: Working group adoption of Loss detection and Congestion Control document
* Chartering + 3 Months: Working group adoption of TLS 1.3 mapping document
* Chartering + 6 Months: Working group adoption of HTTP/2 mapping document
* Chartering + 6 Months: Working group adoption of Multipath extension document
* Chartering + 12 Months: Core Protocol document to IESG
* Chartering + 12 Months: Loss detection and Congestion Control document to IESG
* Chartering + 12 Months: TLS 1.3 Mapping document to IESG
* Chartering + 18 Months: HTTP/2 mapping document to IESG
* Chartering + 18 Months: Multipath extension document to IESG
* Rechartering + 3 Months: Working group adoption of FEC extension document
* Rechartering + 24 Months: FEC extension document to IESG

