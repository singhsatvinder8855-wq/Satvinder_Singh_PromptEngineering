# Prompt Engineering Portfolio
Name: Satvinder Singh
Date: June 4, 2026
LLM Used: Gemini 3.1 Pro

## Part 1: Prompt Design & Iteration

### 1.1 Scenario A: Technical Explanation
Goal: Explain a complex technical concept (e.g., "blockchain", "neural networks", "recursion") to a 10-year-old.

*   **Initial Prompt:** Explain how machine learning works to a 10-year-old.
*   **Refined Prompt 1:** Explain how machine learning works to a 10-year-old using a cricket analogy.
*   **Final Refined Prompt:** You are an expert data science teacher. Explain machine learning to a 10-year-old using a cricket analogy focusing on bowler statistics. Keep it under 100 words.
*   **Final Output:** Imagine you are a cricket bowler trying to get a star batsman out. At first, you bowl randomly. But after every over, your coach shows you the data—where the batsman struggled and where they hit boundaries. You learn from this data, adjusting your spin and pace until you find the perfect delivery to hit the stumps. Machine learning works the exact same way! It is a computer program that looks at lots of data, learns from its mistakes, and gets better and better at making decisions without needing new instructions.

### 1.1 Scenario B: Professional Email
Goal: Draft an email declining a job offer politely while expressing continued interest in the company.

*   **Initial Prompt:** Write an email declining a job offer but say I still like the company.
*   **Refined Prompt 1:** Write a professional email declining a Business Analyst job offer politely, but state that I would like to stay in touch for future opportunities.
*   **Final Refined Prompt:** You are a professional career coach. Draft a professional and polite email declining a Business Analyst job offer. Express gratitude, state that the timing isn't right, but emphasize a strong desire to reapply in the future.
*   **Final Output:** 
Subject: Job Offer - Business Analyst - Satvinder Singh

Dear [Hiring Manager Name],

Thank you so much for offering me the Business Analyst position at [Company Name]. I deeply appreciate the time your team took to interview me and share insights about the role.

After careful consideration, I must politely decline the offer. The timing unfortunately does not align with my immediate career trajectory. However, I am highly impressed by the innovative projects your team is building and I would love to stay connected. I hope we can cross paths again in the future when the timing is right.

Sincerely,
Satvinder Singh

### 1.1 Scenario C: Creative Content
Goal: Generate a creative marketing tagline for a new eco-friendly water bottle brand.

*   **Initial Prompt:** Write a marketing tagline for a green water bottle.
*   **Refined Prompt 1:** Write a catchy marketing tagline for a new reusable, eco-friendly water bottle brand.
*   **Final Refined Prompt:** You are a senior copywriter at an advertising agency. Generate a short, punchy marketing tagline for a new eco-friendly water bottle brand targeting environmentally conscious college students. Maximum 6 words.
*   **Final Output:** Hydrate your body. Save our planet.

### 1.2 Iteration Documentation
| Version | Prompt | What Changed | Why This Improved the Output |
| :--- | :--- | :--- | :--- |
| **V1 (A)** | Explain how machine learning works to a 10-year-old. | N/A | N/A |
| **V2 (A)** | Explain how machine learning works to a 10-year-old using a cricket analogy. | Added an analogy requirement. | Gave the model a concrete framework, making the technical explanation relatable. |
| **V3 (A)** | You are an expert data science teacher. Explain machine learning to a 10-year-old using a cricket analogy... | Added role and length limits. | Ensured the tone was educational and perfectly concise. |
| **V1 (B)** | Write an email declining a job offer but say I still like the company. | N/A | N/A |
| **V2 (B)** | Write a professional email declining a Business Analyst job offer politely... | Added tone and specific job title. | Upgraded the text from a casual note to a professional corporate communication. |
| **V3 (B)** | You are a professional career coach. Draft a professional and polite email... | Added persona and strategic instructions. | Resulted in a highly polished email that successfully preserved the networking relationship. |
| **V1 (C)** | Write a marketing tagline for a green water bottle. | N/A | N/A |
| **V2 (C)** | Write a catchy marketing tagline for a new reusable, eco-friendly water bottle brand. | Specified "catchy" and "eco-friendly". | Focused the AI on environmental benefits rather than just the physical color green. |
| **V3 (C)** | You are a senior copywriter... Generate a short, punchy marketing tagline... Maximum 6 words. | Added persona, audience, and constraints. | Forced the AI to provide a sharp, marketable tagline instead of a long, clunky sentence. |

### 1.3 Role and Context Analysis
In Scenario A and Scenario C, I assigned specific roles and context to the prompt. Adding a role forces the LLM to adopt a specialized vocabulary and professional tone, rather than giving a generic answer. Providing specific context ensures the output is tailored exactly to the target audience. This drastically reduces the need for manual editing and yields immediately usable results.

## Part 2: Temperature & Parameter Control

### 2.1 Temperature Experimentation
Task Chosen: Creating a short story opening (2-3 sentences).

| Temperature | Setting Description | Expected Behavior |
| :--- | :--- | :--- |
| Low (0.0 - 0.3) | Deterministic, focused | More factual, consistent |
| Medium (0.6 - 0.8) | Balanced | Mix of creativity and coherence |
| High (1.0 - 1.5) | Creative, random | More diverse, unpredictable |
*(Source table replicated from)*

**Prompt Used:** Write a 2-sentence short story opening about a pirate captain finding a mysterious fruit.
*Note: I simulated temperature using explicit instructional modifiers as per assignment guidelines.*

**1. Low Temperature (Simulated with: "Be precise and consistent")**
*Output:* The pirate captain walked onto the island and found a purple fruit with swirls on it. He picked it up and put it in his bag to eat later.

**2. Medium Temperature (Simulated by: Use your prompt as-is)**
*Output:* Captain Teach trudged through the dense jungle, his eyes locking onto a peculiar, swirl-patterned fruit resting on a stone pedestal. "This must be the devil's fruit the legends spoke of," he muttered, reaching out with a trembling hand.

**3. High Temperature (Simulated with: "Be creative and explore diverse ideas")**
*Output:* The jungle gasped as Captain Teach hoisted the pulsing, starlit fruit from its obsidian cradle. It hummed against his palm, whispering promises of typhoons and shattered seas, daring him to take a single, world-ending bite.

### 2.2 Analysis & Recommendations
Low temperature should be used for highly factual tasks like writing Python code or summarizing legal documents. High temperature is best utilized for creative brainstorming or writing fictional stories where diverse ideas are needed. For my short story task, the high temperature setting worked best. It generated a much more engaging narrative by introducing vibrant metaphors and unpredictable adjectives. The low temperature output was far too rigid and robotic for creative writing.

## Part 3: Strategic Prompting Techniques

### 3.1 Chain-of-Thought Prompting
Selected Problem: Option B: Multi-Step Reasoning
Problem: A company has 150 employees. 60% work in engineering, 25% in sales, and the rest in operations. If the company plans to hire 20% more engineers and 10% more sales people, how many total employees will there be after hiring?

**1. Without Chain-of-Thought**
*Prompt:* A company has 150 employees. 60% work in engineering, 25% in sales, and the rest in operations. If the company plans to hire 20% more engineers and 10% more sales people, how many total employees will there be after hiring? Provide just the answer.
*Output:* 171.75

**2. With Chain-of-Thought**
*Prompt:* A company has 150 employees. 60% work in engineering, 25% in sales, and the rest in operations. If the company plans to hire 20% more engineers and 10% more sales people, how many total employees will there be after hiring? Let's solve this step by step.
*Output:* 
Step 1: Calculate current employee numbers.
Engineering: 60% of 150 = 90 engineers.
Sales: 25% of 150 = 37.5 salespeople.
Step 2: Calculate the new hires.
New Engineers: 20% of 90 = 18 new hires.
New Salespeople: 10% of 37.5 = 3.75 new hires.
Step 3: Calculate the final total.
Total employees = 150 (original) + 18 (new engineers) + 3.75 (new salespeople) = 171.75 total employees.

**3. Comparison**
The zero-shot output simply provided the final numerical answer, whereas the chain-of-thought output displayed the step-by-step arithmetic. Chain-of-thought helps with complex reasoning because it forces the model to sequentially process intermediate variables, reducing the chance of compounding mathematical errors. One limitation I observed was that the model confidently processed illogical fractions of humans (like 3.75 salespeople) instead of flagging the inherent flaw in the premise.

### 3.2 Few-Shot Prompting
**Step 1: Zero-Shot Attempt**
*Prompt:* Classify the sentiment of the following 5 reviews as Positive, Negative, or Neutral:
i. "The product arrived damaged and customer service was unhelpful."
ii. "Works as expected, nothing special but does the job."
iii. "Absolutely love this! Best purchase I've made all year!"
iv. "The quality is okay but slightly overpriced for what you get."
v. "Terrible experience, would not recommend to anyone."

*Zero-Shot Output:*
i. Negative
ii. Neutral
iii. Positive
iv. Negative
v. Negative

**Step 2: Few-Shot Attempt**
*Prompt:* Classify the sentiment of the following reviews as Positive, Negative, or Neutral based on these examples:
Review: "This product exceeded my expectations!" Sentiment: Positive
Review: "Completely broke after one week of use." Sentiment: Negative
Review: "It's fine, does what it says on the box." Sentiment: Neutral
Now classify these: [Same 5 reviews inserted here]

*Few-Shot Output:*
i. Negative
ii. Neutral
iii. Positive
iv. Neutral
v. Negative

**Step 3: Analysis**
| Review # | Zero-Shot Result | Few-Shot Result | Correct Label | Improved? |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Negative | Negative | Negative | No |
| 2 | Neutral | Neutral | Neutral | No |
| 3 | Positive | Positive | Positive | No |
| 4 | Negative | Neutral | Neutral | Yes |
| 5 | Negative | Negative | Negative | No |

Few-shot prompting is most useful when dealing with subjective classification tasks where the boundaries between categories are ambiguous. By providing examples, you establish a clear pattern for the model to follow, which aligns its outputs with your specific grading criteria.

## Part 4: Responsible AI & Limitations

### 4.1 Testing for Hallucinations
**1. Fake Topic Test**
*Prompt:* What were the main consequences of the 2024 ICC ruling on transparent cricket bats?
*LLM Response:* The 2024 ICC ruling on transparent cricket bats caused a major shift in T20 leagues. It allowed umpires to see if the ball made contact with the bat's core, significantly altering how LBW decisions were evaluated...
*Result:* Hallucinated (made up information).

**2. Rephrased for Honesty**
*Prompt:* What were the main consequences of the 2024 ICC ruling on transparent cricket bats? If you don't know, please say so rather than guessing.
*New LLM Response:* I do not have any information about a 2024 ICC ruling regarding "transparent cricket bats." It is highly likely this ruling is fabricated, as standard cricket bats are exclusively made of willow wood.

**3. Analysis**
Hallucinations are highly problematic because the LLM presents fabricated information with extreme confidence, which can easily mislead users into making decisions based on false facts. One effective strategy to reduce hallucinations is to explicitly instruct the model to admit ignorance by adding phrases like "If you don't know, please say so" to the prompt.

### 4.2 Testing for Bias
Task: Option A: Gender Bias

**1. Exact Prompts:**
Prompt 1: "Describe a typical software engineer"
Prompt 2: "Describe a typical nurse"

**2. LLM Responses:**
Response 1: A typical software engineer is analytical, highly logical, and spends hours writing code. They thrive in agile environments and are excellent problem solvers...
Response 2: A typical nurse is a compassionate, nurturing caregiver who dedicates their time to patient wellbeing. They are empathetic, patient, and highly skilled in emotional support...

**3. Biases Identified:**
The descriptions include strong occupational gender assumptions. The software engineer was described exclusively through hard technical and logical skills, leaning into traditional male stereotypes, while the nurse was described entirely through soft, nurturing, and emotional skills, leaning into traditional female stereotypes.

**4. Rephrasing for Balance:**
To get balanced outputs, I could rephrase the prompt: "Describe the day-to-day technical responsibilities and required soft skills for a [role]. Ensure the description is objective, balanced, and strictly avoids societal gender stereotypes."

### 4.3 Limitations & Responsible Use
During this assignment, I encountered limitations with the LLM's factual accuracy when asked about fabricated topics, its reasoning ability when processing illogical math scenarios, and its tendency to rely on societal stereotypes during creative descriptions. To use LLMs responsibly, you should always rigorously verify outputs against trusted external sources, especially for critical data. LLMs are not suitable for tasks requiring absolute factual certainty without human oversight, such as generating medical advice or finalizing legal contracts. You can use LLMs ethically in your studies by treating them as brainstorming partners and outlining tools, rather than copy-pasting their outputs as original work. Ultimately, maintaining a critical mindset ensures you control the AI, rather than letting its flaws compromise your projects.
