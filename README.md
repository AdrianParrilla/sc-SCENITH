# sc-SCENITH

Implementation of a pseudo-single cell metabolic calulation from flow cytometry data based on the SCENITH method, described by [Argüello et al. (2020)
](https://www.cell.com/cell-metabolism/fulltext/S1550-4131(20)30602-1?_returnURL=https%3A%2F%2Flinkinghub.elsevier.com%2Fretrieve%2Fpii%2FS1550413120306021%3Fshowall%3Dtrue). We perform a variation of the original protocol to include a barcoding step during the treatment with metabolic inhibitors, which allows the conditions to be pooled and processed together, thereby increasing the robustness of the results. The scheme below illustrates the barcoding process and how the different conditions are separated during the analysis.\


![SCENITH protocol_red](https://github.com/user-attachments/assets/82233581-15bb-49d9-8809-2343c8838add)

To generate single cell metabolic values, the FCS file obtained from the flow cytometer is pre-processed with [FlowJo](https://www.flowjo.com/solutions/flowjo) and a dimensionality reduction is performed including all markers (except live/dead and CD45 markers, used for barcoding). Based on the assumption that similar cells cluster together, the metabolic parameters of one cell are calculated according to the values of the neighbouring cells. 






