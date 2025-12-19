---
permalink: /
title: "Welcome to my homepage, have a nice day!"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


**About me**: Hello world! You can call me Quan. Currently, I am an undergrad student at [HUST](https://hust.edu.vn/en/), Vietnam, and also an AI Resident at [Qualcomm AI Research](https://www.qualcomm.com/). I love playing with large language models. I am impressed by the abilities of LLMs, and I am curious about how they work. I want to understand them theoretically.

# Updates

- **[Dec 2025]** I am actively **looking for a PhD position**. Good luck to me!

- **[Jun 2025]** I will attend International Conference on Machine Learning 2025. Let's connect!

- **[May 2025]** I got 2 papers accepted at ICML 2025. What an achievement for me!

- **[Apr 2025]** I officialy joined Qualcomm AI Research as an AI Resident.

- **[Dec 2024]** I achieved an IELTS Academic band score of 7.0!

- **[Aug 2024]** I joined VinAI Research as an AI Resident.

- **[Apr 2024]** My first paper was accepted at ICASSP 2024!


# Research Interests

Despite their impressive emergent abilities [1], Large Language Models (LLMs) are, at their core, massive statistical engines optimizing a conditional probability distribution. The recent history of our field can be viewed as a sequence of attempts to optimize this probability more effectively. Initially, we relied on prompt engineering to provide hand-crafted conditions to guide generation. This evolved into parameter-efficient methods such as prompt-tuning and prefix-tuning, which learn continuous prompt representations to condition the model. As we reached the limits of static conditioning, the frontier shifted to the post-training phase and test-time compute.

However, recent findings [2] suggest that post-training with reinforcement learning (RL) often acts primarily to \textit{sharpen} the conditional probability of the original LLM. This implies that many of the benefits of RL post-training can be approximated by sampling from a power distribution of the base model distribution [3]. In other words, once we scale models sufficiently in both data and parameters, LLMs already possess rich latent abilities, and the challenge becomes how to elicit them reliably. **My research therefore aims to** 
- (i) leverage these intrinsic abilities through robust fine-tuning and test-time compute
- (ii) deepen the scientific understanding of language models by investigating their fundamental statistical properties.

[1]: Emergent Abilities of Large Language Models
[2]: Does reinforcement learning really incentivize reasoning capacity in LLMs beyond the base model?
[3]: Reasoning with sampling: Your base model is smarter than you think












