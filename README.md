# Message Flow Specification Mining for System-on-chip Designs

A system-on-chip (SoC) design can be viewed as being constructed by a large number of blocks that are connected by on-chip 
communcation networks.  System functions are realized by executing those blocks coordinated via system-level protocols. These
protocols specify the types and orderings of messages that are exchanged among system blocks during execution, therefore they
are also referred to as *message flows*. It has been observed that majority of SoC errors can be traced back to or revealed by violations of message flow specifications. Availability of message flow specifications is essential for SoC validation including debug.

We focus on mining patterns about message flows from SoC execution traces.  The goal is to develop methods and algorithms to continuously mine message flow specifications from system execution traces across the entire validation spectrum spanning from pre-silicon to post-silicon stages. The anticipated potential impact is substantial relief of specification requirements on post-silicon debug and improve productivity.

Currently, we are exploring the following two approaching: one based on sequential pattern mining techniques in data mining, and the other using recurrent neural networks (RNNs).

- **Sequential pattern mining**  ---  Basically, this approach considers all sequences of messages (*aka*, events), and identifies those with minimum probability measures over a set of traces as patterns.  Of course, that simple idea is not practical as several challenges have to be addressed: huge search space that leads to high runtime complexity, large number of useless patterns found that can frustrate users, and patterns involved with branching structures that may not be found. We are developing methods and techniques to address them.

- **RNN based mining** --- In this approach, a set of RNNs are trained with SoC execution traces, and they capture sequential dependencies among events.  Once trained, sequential patterns of various lenghts are extracted from those RNNs.  

The following list shows the publications resulting from the above research.

- *Mining Patterns from Concurrent Execution Traces*, MD Rubel Ahmed, H Zheng, P Mukherjee, M Ketkar, Jin Yang, IEEE TCAD, to appear.
- *Model Synthesis for Communication Traces of System Designs*, H Zheng, MD Rubel Ahmed, P Mukherjee, M Ketkar, Jin Yang, ICCD, October, 2021.
- *A Comparative Study of Specification Mining Methods for SoC Communication Traces*, MD Rubel Ahmed, H Zheng, P Mukherjee, M Ketkar, Jin Yang, ISVLSI, July, 2021
- *Mining Message Flows from System-on-Chip Execution Traces*, MD Rubel Ahmed, H Zheng, P Mukherjee, M Ketkar, Jin Yang, ISQED, March, 2021.
- *Mining Message flows using Recurrent Nueral Networks for System-on-chip Design Validation*, Y Cao, P Mukherjee, M Ketkar, Jin Yang, H Zheng, ISQED, March, 2020.
