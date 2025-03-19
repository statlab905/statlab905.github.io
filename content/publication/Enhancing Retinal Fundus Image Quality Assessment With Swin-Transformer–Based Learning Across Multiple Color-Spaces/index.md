---
title: "Enhancing Retinal Fundus Image Quality Assessment With Swin-Transformer–Based Learning Across Multiple Color-Spaces"
authors:
- Chengcheng Huang
- yukang-jiang
- Xiaochun Yang
- Chiyu Wei
- Hongyu Chen
- Weixue Xiong
- Henghui Lin
- xueqin-wang
- Ting Tian
- Haizhu Tan
date: "2024-04-02T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-04-02T00:00:00Z"

publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Translational Vision Science & Technology"
# publication_short: ""

abstract: Purpose:The assessment of retinal image (RI) quality holds significant importance in both clinical trials and large datasets, because suboptimal images can potentially conceal early signs of diseases, thereby resulting in inaccurate medical diagnoses. This study aims to develop an automatic method for Retinal Image Quality Assessment (RIQA) that incorporates visual explanations, aiming to comprehensively evaluate the quality of retinal fundus images (RIs).\n Methods:We developed an automatic RIQA system, named Swin-MCSFNet, utilizing 28,792 RIs from the EyeQ dataset, as well as 2000 images from the EyePACS dataset and an additional 1,000 images from the OIA-ODIR dataset. After preprocessing, including cropping black regions, data augmentation, and normalization, a Swin-MCSFNet classifier based on the Swin-Transformer for multiple color-space fusion was proposed to grade the quality of RIs. The generalizability of Swin-MCSFNet was validated across multiple data centers. Additionally, for enhanced interpretability, a Score-CAM–generated heatmap was applied to provide visual explanations.\n Results:Experimental results reveal that the proposed Swin-MCSFNet achieves promising performance, yielding a micro-receiver operating characteristic (ROC) of 0.93 and ROC scores of 0.96, 0.81, and 0.96 for the “Good,” “Usable,” and “Reject” categories, respectively. These scores underscore the accuracy of RIQA based on Swin-MCSF in distinguishing among the three categories. Furthermore, heatmaps generated across different RIQA classification scores and various color spaces suggest that regions in the retinal images from multiple color spaces contribute significantly to the decision-making process of the Swin-MCSFNet classifier.\n Conclusions:Our study demonstrates that the proposed Swin-MCSFNet outperforms other methods in experiments conducted on multiple datasets, as evidenced by the superior performance metrics and insightful Score-CAM heatmaps.\n Translational Relevance:This study constructs a new retinal image quality evaluation system, which will contribute to the subsequent research of retinal images.

featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://tvst.arvojournals.org/article.aspx?articleid=2793524
---