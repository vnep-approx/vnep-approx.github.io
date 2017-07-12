# Virtual Network Embedding Problem Approximation


## Code documentation

* [vnep-approx](/vnep-approx/)
* [alib](/alib/)


## Overview of scenario generation parameters

| Parameter             | Values                            |
|----------------------:|-----------------------------------|
| Topology              | \{BellCanada, Geant, Uunet\}      |
| Number of Requests    | \{25, 50, 75, 100, 125\}          |
| Exp. number of nodes  | \{5, 6, 7\}                       |
| Neighborhood Size     | \{0.2, 0.3\}                      |
| Node Resource Factor  | \{0.2, 0.4, 0.6, 0.8, 1.0\}       |
| Edge Resource Factor  | \{0.25, 0.5, 1.0, 2.0, 4.0\}      |




## Baseline scenario solutions

Baseline scenario solutions obtained with Integer Program. Each of the heat map squares represents the averaged result of 90 different VNEP instances. Note the different x-axes for the top and the bottom row.

|![](images/evaluation_plots/req_ef/real_req___AXES_NO_REQ_vs_EDGE_RF__.png) | ![](images/evaluation_plots/req_ef/cleaned_embedding_ratio___AXES_NO_REQ_vs_EDGE_RF__.png) |
|----------------------:|-----------------------------------|
| ![](images/evaluation_plots/req_ef/objective_gap___AXES_NO_REQ_vs_EDGE_RF__.png) | ![](images/evaluation_plots/req_ef/runtime___AXES_NO_REQ_vs_EDGE_RF__.png)              |
| ![](images/evaluation_plots/nf_ef/avg_node_load___AXES_RESOURCES__.png) | ![](images/evaluation_plots/nf_ef/max_node_load___AXES_RESOURCES__.png)              |
| ![](images/evaluation_plots/nf_ef/avg_edge_load___AXES_RESOURCES__.png) | ![](images/evaluation_plots/nf_ef/max_edge_load___AXES_RESOURCES__.png)              |

## Scatter Plot

Performance of the randomized rounding algorithm. Out of 250 rounding operations, we depict for each scenario the one solution minimizing resource augmentations (and secondly achieving the highest profit) and the one solution achieving the maximal profit (and secondly minimizing the resource augmentation). The profits of each solution is normalized by the (baseline) profit achieved by the IP. A maximal load y larger than 100% implies that the solution exceeds any of the resources' capacities by y - 100%.

![](images/evaluation_plots/Scatter.png)

## Averaged (over 90 scenarios per square) relative performance of augmentation-free heuristics

<table>
<tr><td><img src="images/evaluation_plots/req_ef/comparison_baseline_rr___AXES_NO_REQ_vs_EDGE_RF__.png"></td><td><img src="images/evaluation_plots/req_ef/comparison_baseline_mdk___AXES_NO_REQ_vs_EDGE_RF__.png"></td></tr>
</table>

## Runtime for the three stages of execution of our approximation algorithm


|![](images/evaluation_plots/req_ef/randround_runtime_pre___AXES_NO_REQ_vs_EDGE_RF__.png) | ![](images/evaluation_plots/req_ef/randround_runtime_opt___AXES_NO_REQ_vs_EDGE_RF__.png) |
|----------------------:|-----------------------------------|
| ![](images/evaluation_plots/req_ef/randround_runtime_post___AXES_NO_REQ_vs_EDGE_RF__.png) | ![](images/evaluation_plots/req_ef/mdk_runtime_total___AXES_NO_REQ_vs_EDGE_RF__.png) |
