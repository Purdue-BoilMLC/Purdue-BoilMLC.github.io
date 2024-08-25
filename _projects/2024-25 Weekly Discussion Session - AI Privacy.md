---
layout: page
title: "AI Privacy"
description: 2024-25 Weekly Discussion Session I
img: "assets/img/event/privacy.webp"
importance: 1
category: "Weekly Discussion"
---
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/event/privacy2.webp" title="Dall-E" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/event/Membership-inference-attack.png" title="MIA" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/event/glaze.png" title="glaze" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


### Discussion Theme: AI Privacy

Artificial Intelligence (AI) promises numerous advancements and conveniences. However, the widespread use of AI technologies raises significant concerns about privacy. From data collection to inference, AI technologies can potentially infringe on individual privacy, posing ethical and legal challenges. This discussion fosters a deeper understanding of these issues, focusing on the balance between innovation and privacy, ethical considerations, and current research advancements in the field of AI privacy.

### Meeting Details

**Time:**  
Every Sunday, 3:00 PM - 4:30 PM EST

**Zoom Link:**  
The Zoom link will be provided to Boil-MLC members via Discord, WeChat or email.

**Language:**  
The discussion will be conducted in English.

**Recording:**  
All sessions will be recorded and made available post-meeting on this page for members to review.

**Reading:**  
Feel free to pick one or two papers provided in the reading list for each week and join the discussion with your ideas and thoughts.


### Syllabus

#### Week 1: Introduction to AI Privacy
- Overview of AI privacy issues focusing on Differentially Private.
- Ethical implications.
- Key challenges and legal perspectives.

**Reading:**
- [Wiki: Differential Privacy](https://en.wikipedia.org/wiki/Differential_privacy)
- [k-anonymity: A model for protecting privacy](https://epic.org/wp-content/uploads/privacy/reidentification/Sweeney_Article.pdf)

#### Week 2: AI Backdoors
- Understanding backdoors in AI systems.
- Methods to detect and prevent backdoors.
- Real-world implications.

**Reading:**
- [BadNL: Backdoor Attacks against NLP Models with Semantic-preserving Improvements](https://arxiv.org/pdf/2006.01043)
- [TrojLLM: A Black-box Trojan Prompt Attack on Large Language Models](https://arxiv.org/pdf/2306.06815)
- [Poisoning and backdooring contrastive learning](https://arxiv.org/pdf/2106.09667)
- [BadEncoder: Backdoor Attacks to Pre-trained Encoders in Self-Supervised Learning](https://arxiv.org/pdf/2108.00352)
- [Distribution preserving backdoor attack in self-supervised learning](https://www.cs.purdue.edu/homes/taog/docs/SP24.pdf)
- [Dual-Key Multimodal Backdoors for Visual Question Answering](https://arxiv.org/pdf/2112.07668)
- [BACKDOORL: Backdoor Attack against Competitive Reinforcement Learning](https://arxiv.org/pdf/2105.00579)
- [Backdooring Neural Code Search](https://arxiv.org/pdf/2305.17506)
- [Towards reliable and efficient backdoor trigger inversion via decoupling benign features](https://openreview.net/pdf?id=Tw9wemV6cb)
- [Elijah: Eliminating backdoors injected in diffusion models via distribution shift](https://arxiv.org/pdf/2312.00050)
- [ODSCAN: Backdoor Scanning for Object Detection Models](https://www.cs.purdue.edu/homes/cheng535/static/papers/sp24_odscan.pdf)
- [Unicorn: A unified backdoor trigger inversion framework](https://arxiv.org/abs/2304.02786)
- [Detecting backdoors in pre-trained encoders](https://arxiv.org/pdf/2303.15180)
- [Detecting AI trojans using meta neural analysis](https://arxiv.org/pdf/1910.03137)
- [ASSET: Robust backdoor data detection across a multiplicity of deep learning paradigms](https://www.usenix.org/system/files/usenixsecurity23-pan.pdf)
- [Reconstructive neuron pruning for backdoor defense](https://arxiv.org/pdf/2305.14876)
- [UNIT: Backdoor Mitigation via Automated Neural Distribution Tightening](https://arxiv.org/pdf/2407.11372)
- [Exploring the Orthogonality and Linearity of Backdoor Attacks](https://kaiyuanzhang.com/publications/SP24_Backdoor.pdf)

#### Week 3: LLM Jailbreaking
- Techniques and challenges in LLM jailbreaking.
- Security concerns and mitigation strategies.
- Case studies and examples.

**Reading:**
- ["Do Anything Now": Characterizing and Evaluating In-The-Wild Jailbreak Prompts on Large Language Models](https://arxiv.org/abs/2308.03825)
- [Tricking LLMs into Disobedience: Understanding, Analyzing, and Preventing Jailbreaks](https://arxiv.org/abs/2305.14965)
- [Jailbreaking ChatGPT via Prompt Engineering: An Empirical Study (NDSS 2024)](https://arxiv.org/abs/2305.13860)
- [Survey of Vulnerabilities in Large Language Models Revealed by Adversarial Attacks](https://arxiv.org/pdf/2310.10844.pdf)

#### Week 4: Membership Inference Attacks on Classification Models
- Understanding membership inference attacks.
- Privacy risks associated with classification models.
- Defense mechanisms.

**Reading:**
- [Membership Inference Attacks on Machine Learning: A Survey](https://arxiv.org/pdf/2103.07853v4)
- [Membership Inference Attacks Against Machine Learning Models](https://arxiv.org/pdf/1610.05820v2)
- [Membership Inference Attacks From First Principles](https://arxiv.org/pdf/2112.03570v2)
- [MIST: Defending Against Membership Inference Attacks Through Membership-Invariant Subspace Training](https://arxiv.org/pdf/2311.00919)
- [Efficient Privacy Auditing in Federated Learning](https://www.usenix.org/system/files/usenixsecurity24-chang.pdf)

#### Week 5: Machine Unlearning
- Concept and necessity of machine unlearning.
- Techniques and challenges.
- Potential applications and future directions.

**Reading:**
- [Learning to Unlearn: Instance-wise Unlearning for Pre-trained Classifiers](https://arxiv.org/abs/2301.11578)
- [Fast Machine Unlearning Without Retraining Through Selective Synaptic Dampening](https://arxiv.org/abs/2308.07707)
- [Separate the Wheat from the Chaff: Model Deficiency Unlearning via Parameter-Efficient Module Operation](https://arxiv.org/abs/2308.08090)
- [Towards Effective and General Graph Unlearning via Mutual Evolution](https://arxiv.org/abs/2401.11760)
- [Backdoor Attacks via Machine Unlearning](https://ojs.aaai.org/index.php/AAAI/article/view/29321)
- [RRL: Recommendation Reverse Learning](https://ojs.aaai.org/index.php/AAAI/article/view/28782)
- [SIFU: Sequential Informed Federated Unlearning for Efficient and Provable Client Unlearning in Federated Optimization](https://arxiv.org/abs/2211.11656)
- [Forgetting User Preference in Recommendation Systems with Label-Flipping](https://ieeexplore.ieee.org/abstract/document/10386603/authors#authors)
- [FedCIO: Efficient Exact Federated Unlearning with Clustering, Isolation, and One-shot Aggregation](https://ieeexplore.ieee.org/document/10386788)
- [Machine Unlearning for Image-to-Image Generative Models](https://openreview.net/forum?id=9hjVoPWPnh)
- [Label-Agnostic Forgetting: A Supervision-Free Unlearning in Deep Models](https://openreview.net/forum?id=SIZWiya7FE)
- [Ring-A-Bell! How Reliable are Concept Removal Methods for Diffusion Models?](https://arxiv.org/abs/2310.10012)
- [A Unified and General Framework for Continual Learning](https://openreview.net/forum?id=BE5aK0ETbp)
- [Rethinking Adversarial Robustness in the Context of the Right to be Forgotten](https://icml.cc/virtual/2024/poster/32857)
- [Machine Unlearning in Learned Databases: An Experimental Analysis](https://arxiv.org/abs/2311.17276)
- [CaMU: Disentangling Causal Effects in Deep Model Unlearning](https://epubs.siam.org/doi/abs/10.1137/1.9781611978032.89)
- [Learn To Unlearn for Deep Neural Networks: Minimizing Unlearning Interference With Gradient Projection](https://openaccess.thecvf.com/content/WACV2024/html/Hoang_Learn_To_Unlearn_for_Deep_Neural_Networks_Minimizing_Unlearning_Interference_WACV_2024_paper.html)
- [On the Effectiveness of Unlearning in Session-Based Recommendation](https://dl.acm.org/doi/abs/10.1145/3616855.3635823)
- [Graph Unlearning with Efficient Partial Retraining](https://dl.acm.org/doi/abs/10.1145/3589335.3651265)
- [ERASER: Machine Unlearning in MLaaS via an Inference Serving-Aware Approach](https://arxiv.org/abs/2311.16136)
- [Brainwash: A Poisoning Attack to Forget in Continual Learning](https://arxiv.org/abs/2311.11995)
- [Challenging Forgets: Unveiling the Worst-Case Forget Sets in Machine Unlearning](https://arxiv.org/abs/2403.07362)
- [Scissorhands: Scrub Data Influence via Connection Sensitivity in Networks](https://arxiv.org/abs/2401.06187)
- [To Generate or Not? Safety-Driven Unlearned Diffusion Models Are Still Easy To Generate Unsafe Images ... For Now](https://arxiv.org/abs/2310.11868)
- [How to Forget Clients in Federated Online Learning to Rank?](https://arxiv.org/abs/2401.13410)
- [SalUn: Empowering Machine Unlearning via Gradient-based Weight Saliency in Both Image Classification and Generation](https://openreview.net/forum?id=gn0mIhQGNM)
- [Tangent Transformers for Composition, Privacy and Removal](https://openreview.net/forum?id=VLFhbOCz5D)

#### Week 6: Alignment and Generated Content Detection
- Ensuring AI alignment with human values.
- Challenges in detecting AI-generated content.
- Ethical considerations.

**Reading:**
- [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/pdf/2307.15043)
- [On Large Language Models' Resilience to Coercive Interrogation](https://www.cs.purdue.edu/homes/cheng535/static/papers/sp24_lint.pdf)
- [AutoDAN: Generating Stealthy Jailbreak Prompts on Aligned Large Language Models](https://openreview.net/pdf?id=7Jwpw4qKkb)
- [How johnny can persuade llms to jailbreak them: Rethinking persuasion to challenge ai safety by humanizing llms](https://arxiv.org/pdf/2401.06373)
- [CNN-Generated Images Are Surprisingly Easy to Spot... for Now](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_CNN-Generated_Images_Are_Surprisingly_Easy_to_Spot..._for_Now_CVPR_2020_paper.pdf)
- [Leveraging Frequency Analysis for Deep Fake Image Recognition](https://proceedings.mlr.press/v119/frank20a/frank20a.pdf)
- [Towards Universal Fake Image Detectors That Generalize Across Generative Models](https://openaccess.thecvf.com/content/CVPR2023/papers/Ojha_Towards_Universal_Fake_Image_Detectors_That_Generalize_Across_Generative_Models_CVPR_2023_paper.pdf)
- [DIRE for Diffusion-Generated Image Detection](https://openaccess.thecvf.com/content/ICCV2023/papers/Wang_DIRE_for_Diffusion-Generated_Image_Detection_ICCV_2023_paper.pdf)
- [DRCT: Diffusion Reconstruction Contrastive Training towards Universal Detection of Diffusion Generated Images](https://openreview.net/pdf?id=oRLwyayrh1)
- [GLTR: Statistical Detection and Visualization of Generated Text](https://aclanthology.org/P19-3019.pdf)
- [DetectGPT: Zero-shot Machine-Generated Text Detection using Probability Curvature](https://proceedings.mlr.press/v202/mitchell23a/mitchell23a.pdf)
- [RADAR: Robust Ai-Text Detection via Adversarial Learning](https://proceedings.neurips.cc/paper_files/paper/2023/file/30e15e5941ae0cdab7ef58cc8d59a4ca-Paper-Conference.pdf)
- [DetectLLM: Leveraging Log Rank Information for Zero-Shot Detection of Machine-Generated Text](https://aclanthology.org/2023.findings-emnlp.827.pdf)
- [Fast-DetectGPT: Efficient Zero-Shot Detection of Machine-Generated Text via Conditional Probability Curvature](https://openreview.net/pdf?id=Bpcgcr8E8Z)
- [Raidar: geneRative AI Detection viA Rewriting](https://openreview.net/pdf?id=bQWE2UqXmf)
- [Spotting LLMs With Binoculars: Zero-Shot Detection of Machine-Generated Text](https://openreview.net/pdf?id=axl3FAkpik)

#### Week 7 and Beyond: Paper Readings and Open Discussion
- After the initial weeks, we will transition to reading and discussing seminal papers and emerging research in AI privacy.
- Each week, members will be assigned a paper to read followed by an open discussion.

### Policies

- **Attendance:** Only Boil-MLC members can attend live sessions.
- **Participation:** Active participation is encouraged to foster a collaborative learning environment.
- **Recording Access:** Recordings of sessions will be posted on this page after each meeting for those who missed the live discussion.
- **Confidentiality:** Discussions are for educational purposes only. Sharing of sensitive or proprietary information is discouraged.
- **Respect and Inclusivity:** All participants are expected to maintain a respectful and inclusive atmosphere during discussions.

### Join Us

For a comprehensive understanding of AI privacy and to engage with a passionate community, join our weekly discussions. Stay informed, stay ethical, and contribute to the future of AI.

### Credits
- https://www.researchgate.net/figure/Membership-inference-attack_fig1_339897331
- https://www.youtube.com/watch?v=WpHkTVb3CUg