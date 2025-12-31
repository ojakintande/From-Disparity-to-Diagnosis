Algorithmic fairness interventions often focus on quantifying and mitigating aggregate outcome disparities, yet they lack explanatory
power for how these disparities arise during model training. This work bridges the gap between outcome-based fairness auditing
and training-data-centric interpretability by introducing a diagnostic framework grounded in group-level influence functions. We
decompose the total influence on a demographic group’s predictions into two novel components: self-influence (intra-group) and
between-influence (inter-group). This decomposition reveals two critical failure modes: stereotyping, driven by disproportionate interinfluence from perceived advantaged groups, and under-learning, caused by insufficient self-influence within a perceived disadvantaged
group. We theoretically link these components to violations of standard group fairness criteria. Through an experimental case study on
the COMPAS recidivism dataset, we demonstrate that the most severe fairness violations are frequently driven by strong intra-group
influence. This finding challenges the conventional inter-group debiasing paradigms. Following influence-based diagnosis and targeted
data reweighting, we employ SHAP to provide interpretable, feature-level explanations of residual bias. This end-to-end pipeline,
diagnosing disparity origins via self- and between-influence, followed by targeted mitigation via valid statistical tests and explainable
audit, moves beyond documenting what disparities exist to diagnosing or auditing how they emerge, enabling more precise and
effective bias interventions in high-stakes domains
