+++
categories = []
tags = []
date = "2013-11-30"
title = "Our Research"
+++
# Our Research

During its growth and division cycle the cell replicates all of its components and distributes them to create two daughter cells [1]. It is essential that the underlying processes, DNA replication (S phase), mitosis (M phase) and cell division (CD), take place in a defined sequence with the correct temporal separation: G1 → S → G2 → M → CD → G1 → . Progression through this sequence is characterized by specific transitions at boundaries between sequential stages of the cell cycle. At the **Restriction point** in G1 phase the cell decides whether to proliferate or quiesce (G0). This is followed later by the abrupt **G1/S transition** into S phase (DNA replication). Post-replicative cells in G2 phase enter into mitosis (M phase) at the **G2/M transition**. The decision to segregate sister-chromatids once all have become aligned pairwise on the mitotic spindle takes place at the end of prometaphase and triggers the **meta/anaphase transition and cytokinesis**. Anaphase is followed by the exit from mitosis back into G1 (mitotic exit). Progression through the cell cycle in eukaryotes is controlled by a conserved protein interaction network composed of protein kinases and phosphatases with stoichiometric inhibitors and activators, transcription factors, ubiquitin-conjugating enzymes and the proteasome. The molecular interactions among these cell cycle regulators create a complicated **dynamical system** that oscillates once per cell cycle. In our proposal we focus on a systems-level description of the major cell cycle transitions in the mammalian cell cycle. Our **hypothesis-driven** research is based on our theoretical investigations of generic dynamic characteristics in eukaryotic cell cycle transitions.

{{< figure src="https://novakgroupoxford.github.io/bicycle-hugo/img/activator-inhibitor.png" title="Fig.1: Generic network motif of cell cycle transitions"  class="img-post">}}
*The three components are embedded in a negative feedback loop. The antagonism between Activator<sub>i</sub> and Inhibitor<sub>i</sub> creates a positive circuit.*

Progression through each of the cell cycle transitions is controlled by a balance between **inhibitors** and **activators** (Fig.1). Before each cell cycle transition, an inhibitor overwhelms the activator responsible for the transition (refered here as **Inhibitor<sub>i</sub>** and **Activator<sub>i</sub>**). During the transition Inhibitor<sub>i</sub> gets down-regulated by the activator of the previous cell cycle stage (Activator<sub>i-1</sub>) which leads to activation of Activator<sub>i</sub>. However after the transition, Activator<sub>i</sub> inhibits the activator characteristic for the earlier cell cyle stage (Activator<sub>i-1</sub>), which creates a **negative feedback loop** in the network [2]. The **irreversibility** of cell cycle transitions requires that Inhibitor<sub>i</sub> is kept inactive in the post-transition state despite the disappearance of Activator<sub>i-1</sub>. We argue that the irreversibility of the cell cycle transition is achieved by an **antagonistic interaction** between Activator<sub>i</sub> and its cognate Inhibitor<sub>i</sub>. This **double-negative feedback** makes the post-transition state and Activator<sub>i</sub> self-maintaining by creating a **bistable switch** (Fig.2). The irreversible switch creates a **‘point of no return’** in the cell cycle transition, which can be experimentally tested by the following protocol. In a partly synchronised cell population undergoing the transition, abrupt inactivation of Activatori-1 redirects cells back to the bistable region close to the y-axis. The future cellular fate will be dependent upon whether cells end up above or below the unstable saddle point (Fig.3). Cells early in the transition will return to the pre-transition cell cycle state (cell ) with low Activator<sub>i</sub> and high Inhibitor<sub>i</sub> levels. In contrast, cells later in the transition will manage to reach the post-transition (i) state (cell ) where the levels of Activator<sub>i</sub> and Inhibitor<sub>i</sub> are the opposite.

{{< figure src="https://novakgroupoxford.github.io/bicycle-hugo/img/phaseplane.png" title="Fig.2: Two phaseplane portraits of the generic cell cycle switch"  class="img-post">}}
*At small Activator<sub>i-1</sub> levels the network has two alternative steady states (solid lines) separated by unstable saddle points (dashed lines). The trajectories are shown by dotted curves.*

The sequential connection of these switch-like network motifs not only accounts for oscillations of activators and inhibitors during cell cycle progression, but also provides **‘checkpoint’** control over the cell cycle transitions. By monitoring defective states of chromosomes (damaged, not fully replicated, or improperly aligned on the mitotic spindle), intracellular surveillance mechanisms keep Activator<sub>i-1</sub> at a subthreshold level and thereby block the transition. When the defect is repaired, the bistable switch is released to drive the transition as shown (Fig.2).

{{< figure src="https://novakgroupoxford.github.io/bicycle-hugo/img/bistability.png" title="Fig.3: The bistable switch creates a ‘point of no return’"  class="img-post">}}
*Depletion of the initial activator (Activator<sub>i-1</sub>) during the transition bifurcates the cell population.*

Our view of eukaryotic cell cycle control is based on years of experience modelling the cell cycle of organisms like budding [3] and fission [4] yeasts, Xenopus [5] and Drosophila [6] embryos. Our prediction that eukaryotic cell cycle transitions are controlled by underlying bistable network motifs has been tested and confirmed experimentally (by the research groups of Cross, Ferrell, Sible, Morgan and Uhlmann) for each cell cycle transition of lower eukaryotes (yeasts and Xenopus embryos). However it remains elusive, whether these same **design principles** are applicable to higher eukaryotic cells with more complex cell cycle control networks. Although there is strong evidence for the universality of eukaryotic cell cycle components, the physiological characteristics of the cell cycle vary widely across cell types. This raises the question whether the control mechanisms are conserved or not? A systematic analysis of bistable and other network motifs in mammalian cell cycle transitions is essential to address this question.

According to our working hypothesis, mammalian cell cycle progression is driven by a **series of bistable switches** connected in a linear sequence (Fig.4). The activators of early cell cycle transitions (from the Restriction Point to the G2/M transition) belong to the Cyclin-dependent protein-kinase (**Cdk**) family (Cdk1, Cdk2, Cdk4, Cdk6 etc.) in complex with their regulatory **Cyclin** subunits (Cyclin-A, -B, -D, -E etc.). During the cell cycle, Cdks are periodically associated with their activating Cyclins whose levels are determined by transcription factors (e.g. E2F) and degradation machineries (ubiquitin-ligases: SCF and APC/C). The activity of Cdk:Cyclin complexes is subject to additional controls by stoichiometric Cdk inhibtors (e.g. p27<sup>Kip1</sup>), inhibitory phosphorylations modulated by Wee1-kinases and Cdc25-phosphatases. The different activators and inhibitors of mammalian cell cycle transitions are summarised in the Table and the experimental evidence for potential bistable network motifs operating at cell cycle transitions are briefly summarised below:

{{< figure src="https://novakgroupoxford.github.io/bicycle-hugo/img/motif.png" title="Fig.4: The sequential activation of bistable switches during mammalian cell cycle progression" class="img-post">}}
*The antagonistic relationships between cell cycle activators and inhibitors are illustrated as an auto-activation of activators, for simplicity.*

**Restriction Point (RP)** is enforced by the Retinoblastoma Protein (pRb), a repressor of E2F transcription factors. pRb is inactivated by CycE-dependent kinase via a positive feedback loop:
E2F → CycE
 ¬ Rb ¬ E2F. The RP is the only cell cycle transition in mammalian cells where bistability has been experimentally demonstrated [7].

**G1/S transition** is triggered by CycE-kinase which turns off degradation of CycA by APC/C<sup>Cdh1</sup> and promotes degradation of the Cdk2 inhibitor p27<sup>Kip1</sup> (double-negative feedback). CycE levels are down-regulated after the transition by activities of Cdk2 (negative feedback) [8,9].

**G2/M transition** is facilitated by CycA-kinase turning off the degradation of CycB through inactivation of APC/CCdh1 and by reducing the extent of inhibitory phosphorylation of Cdk1:CycB complexes and PP2A:B55 activity. Once activated, CycB-kinase is able to prevent this inhibitory phosphorylation (positive feedback). CycB also promotes APC/C<sup>Cdc20</sup> dependent destruction of CycA (negative feedback) by a SAC independent mechanism without destabilizing the mitotic state.

**Meta/anaphase transition** is initiated by APC/C<sup>Cdc20</sup> whose activation requires CycB dependent phosphorylation. APC/C<sup>Cdc20</sup> triggers anaphase by promoting the degradation of Separase inhibitors, Securin and CycB (negative feedback). However APC/C activity is blocked by the Mitotic Checkpoint Complex (MCC) which is inactivated by APC/C dependent ubiquitylation10 (double-negative feedback).

**Mitotic exit** includes the activation of PP2A:B55 phosphatase which counteracts the inhibitory phosphorylations by Cdk1:CycB on the cytokinesis machinery. Since PP2A:B55 is kept inactive during mitosis by its stoichiometric inhibitors (Endosulfine, Arpp19) in a CycB-kinase dependent manner, its initial activation requires CycB degradation by APC/C<sup>Cdc20</sup>. We have proposed11 that PP2A:B55 promotes its own activation by inactivating Greatwall-kinase (positive feedback).


### Activators and inhibitors of mammalian cell cycle transitions.

<div class="row text-center">
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-naq5{font-weight:bold;font-family:"Courier New", Courier, monospace !important;;text-align:center;vertical-align:top}
.tg .tg-r5us{font-family:"Courier New", Courier, monospace !important;;text-align:center;vertical-align:top}
</style>
<table class="tg" align="center">
  <tr>
    <th class="tg-naq5">Cell Cycle Transition</th>
    <th class="tg-naq5">Inhibitors</th>
    <th class="tg-naq5">Activators</th>
  </tr>
  <tr>
    <td class="tg-r5us">Restriction point</td>
    <td class="tg-r5us">Retinoblastoma Protein (pRb)</td>
    <td class="tg-r5us">Cdk4,6:CycD,Cdk2:CycE, E2F</td>
  </tr>
  <tr>
    <td class="tg-r5us">G1/S</td>
    <td class="tg-r5us">p27:Kip1, APC/C:Cdh1</td>
    <td class="tg-r5us">Cdk2:CycE, Cdk2:CycA</td>
  </tr>
  <tr>
    <td class="tg-r5us">G2/M</td>
    <td class="tg-r5us">Wee1, Myt1, PP2A:B55</td>
    <td class="tg-r5us">Cdk1:CycB, Cdk1:CycA, Cdc25</td>
  </tr>
  <tr>
    <td class="tg-r5us">Meta/Anaphase</td>
    <td class="tg-r5us">Mitotic Checkpoint Comples (MCC)</td>
    <td class="tg-r5us">Anaphase Promoting Complex/Cyclosome (APC/C)</td>
  </tr>
  <tr>
    <td class="tg-r5us">Mitotic Exit</td>
    <td class="tg-r5us">Cdk1:CycB, Endosulfine (Arpp19), Greatwall-kinase</td>
    <td class="tg-r5us">PP2A:B55, Polo-kinase, Aurora-kinases</td>
  </tr>
</table>
</div>


### Funded by the BBSRC grant number BB/M00354X/1

## References

1 Morgan, D. O. The Cell Cycle: Principles of Control., (New Science Press, 2007).

2 Verdugo, A., Vinod, P. K., Tyson, J. J. & Novak, B. Molecular mechanisms creating bistable switches at cell cycle transitions. Open biology 3, 120179, doi:10.1098/rsob.120179 (2013).

3 Chen, K. C. et al. Kinetic analysis of a molecular model of the budding yeast cell cycle. Mol Biol Cell 11, 369-391 (2000).

4 Novak, B. & Tyson, J. J. Modeling the control of DNA replication in fission yeast. Proc Natl Acad Sci U S A 94, 9147-9152 (1997).

5 Novak, B. & Tyson, J. J. Numerical analysis of a comprehensive model of M-phase control in Xenopus oocyte extracts and intact embryos. J Cell Sci 106, 1153-1168 (1993).

6 Calzone, L., Thieffry, D., Tyson, J. J. & Novak, B. Dynamical modeling of syncytial mitotic cycles in Drosophila embryos. Mol Syst Biol 3, 131 (2007).

7 Yao, G., Lee, T. J., Mori, S., Nevins, J. R. & You, L. A bistable Rb-E2F switch underlies the restriction point. Nat Cell Biol 10, 476-482 (2008).

8 Kalaszczynska, I. et al. Cyclin A is redundant in fibroblasts but essential in hematopoietic and embryonic stem cells. Cell 138, 352-365, doi:10.1016/j.cell.2009.04.062 (2009).

9 Krek, W. et al. Negative regulation of the growth-promoting transcription factor E2F-1 by a stably bound cyclin A-dependent protein kinase. Cell 78, 161-172 (1994).

10 Musacchio, A. & Ciliberto, A. The spindle-assembly checkpoint and the beauty of self-destruction. Nat Struct Mol Biol 19, 1059-1061, doi:10.1038/nsmb.2429 (2012).

11 Hegarat, N. et al. PP2A/B55 and Fcp1 regulate Greatwall and Ensa dephosphorylation during mitotic exit. PLoS Genet 10, e1004004, doi:10.1371/journal.pgen.1004004 (2014).
