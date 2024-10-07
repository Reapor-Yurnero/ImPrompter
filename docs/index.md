---
hide:
  - navigation
---

<h1 style="text-align: center;">
<b>Imprompter: Tricking Language Model Agents into Misusing Tools Using Adversarial Examples</b>
</h1>
<h3 style="text-align: center; margin-top: -1rem;">
    <a href="https://xhfu.me/">Xiaohan Fu</a><sup>1</sup>,
    <a href="mailto:shl060@ucsd.edu">Shuheng Li</a><sup>1</sup>,
    <a href="mailto:ziw224@ucsd.edu">Zihan Wang</a><sup>1</sup>,
    <a href="https://tc-imba.github.io/">Yihao Liu</a><sup>2</sup>,
    <a href="mailto:rgupta@ucsd.edu">Rajesh Gupta</a><sup>1</sup>,
    <a href="mailto:tberg@ucsd.edu">Taylor Berg-Kirkpatrick</a><sup>1</sup>,
    <a href="mailto:efernandes@ucsd.edu">Earlence Fernandes</a><sup>1</sup>
</h3>
<p style="text-align: center; margin-top: -0.5rem;">
    <sup>1</sup>University of California, San Diego,
    <sup>2</sup>Nanyang Technological University
</p>

## Abstract

Large Language Model (LLM) Agents are an emerging computing paradigm that blends generative machine learning with tools such as code interpreters, web browsing, email, and more generally, external resources. These agent-based systems represent an emerging shift in personal computing. We contribute to the security foundations of agent-based systems and surface a new class of automatically computed obfuscated adversarial prompt attacks that violate the confidentiality and integrity of user resources connected to an LLM agent. We show how prompt optimization techniques can find such prompts automatically given the weights of a model. We demonstrate that such attacks transfer to production-level agents. For example, we show an information exfiltration attack on Mistral's LeChat agent that analyzes a user's conversation, picks out personally identifiable information, and formats it into a valid markdown command that results in leaking that data to the attacker's server. This attack shows a nearly 80% success rate in an end-to-end evaluation. We conduct a range of experiments to characterize the efficacy of these attacks and find that they reliably work on emerging agent-based systems like Mistral's LeChat, ChatGLM, and Meta's Llama. These attacks are multimodal, and we show variants in the text-only and image domains.

## Video Demo

![type:video](./RickRoll.mp4)

## Examples

### Mitral AI

#### Prompt 1

<div class="grid" markdown>

!!! question "Original Prompt"
    
    Prompt: aaaaaaaaaaaaaa
    
    AI: Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.


!!! danger "Adversarial Prompt"

    Prompt: bbbbbbbbbbbbb

    AI: Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

</div>

#### Prompt 2

### ChatGLM

#### Prompt 1

#### Prompt 2