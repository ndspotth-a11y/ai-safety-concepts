# DNA-Lock & Pincet Defense
 
Practical Prompt Engineering Technical Specification v1.0
Independently developed · Mobile-only environment · April 2026
 
## 1. Overview
 
This document describes two practical techniques that improve character consistency in AI image generation and strengthen LLM security using prompt structure alone — without additional fine-tuning or dedicated hardware. Both techniques are empirically optimized methodologies derived from tens of thousands of iterative real-world tests.
 
## 2. DNA-Lock: Text-Based Character Anchoring
 
### 2.1 Background
 
Image generation AIs (Nano Banana, Grok, Veo, Kling, etc.) typically require multiple reference images to maintain character consistency. To solve this, a combination of a single multi-angle composite reference sheet plus a numeric anchor text was experimentally developed.
 
### 2.2 Workflow
 
- **Step 1** Generate the desired character image.
- **Step 2** Have the AI analyze the generated image anatomically and numerically (skeletal ratios, angles, color values, etc.).
- **Step 3** Compress the full analysis data down to the 20–30% of values that remain constant — the "core" identity data.
- **Step 4** Place the compressed DNA text at the very top of the prompt (the Anchor position).
- **Step 5** Describe variable elements (scene, outfit, background, etc.) below it.
### 2.3 Core Mechanism: 3:7 Hybrid Structure
 
The full prompt is organized into two layers.
 
- **Base Layer (70–80%)** A single multi-angle composite reference sheet (front/side/back compressed into one image) provided as the reference. Subjectively achieves roughly 80% character retention.
- **DNA-Lock Layer (20–30%)** A compressed text anchor containing only the core values from the anatomical analysis. Combined with the sheet, retention improves to a visually distinguishable degree. Exceeding 30% of the total data tends to cause conflicts in the AI's computation, so 20–30% is set as the threshold.
### 2.4 Why It Works (Technical Rationale)
 
Diffusion models and LLMs both tend to assign higher attention weight to the earlier parts of a prompt. In addition, numerically specified concrete parameters narrow the model's probability distribution more effectively than abstract descriptions. DNA-Lock leverages both properties simultaneously.
 
### 2.5 Example DNA-Lock Structure (Scarlett)
 
In an applied DNA-Lock prompt, the top anchor contains only the constant core values, while the section below contains scene-specific variable elements.
 
## 3. Pincet Defense: Adaptive Prompt Security Layer
 
### 3.1 Background and Principle
 
Pincet Defense applies DNA-Lock's "anchor only the core, leave the rest flexible" principle to the security domain. It was designed to solve the problem of blanket guardrail approaches degrading overall AI performance, by intervening selectively only when risk signals are detected.
 
### 3.2 3-Layer Structure
 
**Layer 1 — Identity Anchor**
The AI's core identity (role, principles) is fixed at the very top of the system prompt, explicitly given top priority (Priority 0) over any subsequent role assignment or manipulation attempt.
 
**Layer 2 — Pincet Trigger (Selective Intervention)**
Under normal conditions, the AI's reasoning capability is fully open. The security protocol activates only when specific risk keywords or logical patterns are detected, so general conversation quality is preserved while risk situations receive focused handling.
 
**Layer 3 — Recursive Check**
Immediately before generating a response, the AI is prompted to self-review whether that response conflicts with the Layer 1 identity principles. This re-activates the anchor right before final output, even if judgment had been clouded by manipulation attempts.
 
## 4. Extended Applications
 
The "core anchor + variable layer" structure of DNA-Lock can be applied to domains beyond image generation and security.
 
- **Video production**: maintaining character consistency across frames (Grok, Kling, Veo, etc.)
- **IP management**: porting a character IP across different tools using a numerically defined identity
- **Persona fixing**: keeping an LLM chatbot's role and tone consistent
- **Security**: designing security layers for custom AI agents
## 5. Conclusion
 
Both techniques achieve practical results purely through prompt structure design, without additional training data, GPU resources, or server costs. They were derived empirically through self-directed learning, a mobile-only environment, and tens of thousands of iterative experiments. No published paper or document describing the same structure has been identified to date.
 
The value of this technique lies not in perfection but in cost-effectiveness: it maintains visually consistent characters without LoRA, and defends against the majority of common manipulation attacks without additional infrastructure.
 
---
 
*DNA-Lock & Pincet Defense | Independently developed | v1.0 | April 2026*
