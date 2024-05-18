Let us consider our AI hackathon title as "LLM Prompt Recovery", a Kaggle competition with a award of $200,000. 

**Title description:** LLMs are commonly used to rewrite or make stylistic changes to text. The goal of this competition is to recover the LLM prompt that was used to transform a given text.

-----

### Week 1 and 2: Problem Formulation, Data Acquisition and Preprocessing
**Day 1-2:** Form a potential team with focused interest on this topic. Understand the theme and problem statements of the hackathon. 
**Day 3-4:** Formulate the problem statement quantitatively. This competition already mentioned the metrics for evaluation as  Sharpened Cosine Similarity. If the metrics are not define, formulate one based on the task.

This phase also include: 

1. Team Collaboration: Maintain regular communication within the team. Assign roles and responsibilities based on individual strengths.
2. Compute Resources: Estimate the computational requirements for training and inference. Utilize cloud platforms or GPU instances if needed.
3. API: Look for open source system, if not look for nominal fee API keys.
4. Version Control: Use version control systems like Git to manage codebase and track changes.

**Day 5-10:** Since it is NLP problem, we can use LLM to create synthetic dataset. Here, the data can be generated using the LLM by passing an original text and a prompt in order to modify the original text in some desired way as mentioned in prompt. The output is rewritten text or modified original text as per prompt.

Steps to create dataset:
1. We need diverse prompts, so collect prompt templates from internet which specifically says LLM to rewrite a given text.
2. Take few essays available in the internet on which the prompt will be applied. 
3. Prompt the LLM using the created prompt, text pair and collect the output given by LLM. 

**Day 11-14:** Clean the acquired datasets. Handle missing values, outliers, and inconsistencies. 

Things to take care:

The model may start a response, "Sure, I can rewrite that as ____________" which will essentially put the prompt in the generated response. Edit this out because otherwise it would be too easy.
 "too violent" or "against the policies" response by the model should be taken care. 

### Week 3 and 4: Model Selection, Training, Evaluation and Deployment
**Day 15-16:** After generating data, you need to train a model to predict the rewrite_prompt by inputting the original_text and the rewritten_text to the model

**Day 17-18:** Split the data into training, validation, and test sets. 

**Day 19-24:** Fine tune baseline LLM models using default parameters on the collected data. Evaluate their performance using chosen metrics. Iterate on model selection and hyperparameter tuning.

**Day 25-26:** Validate the final model(s) on the test set to assess generalization performance.
For evaluation, we actually need to generate embeddings, a lower-dimensional semantic representation of our text. This embedding is generated using the sentence embedding model. So we pass our predicted rewritten_prompt and the corresponding true rewritten_prompt to this model and get both embeddings. Once you have the embeddings you need to compare them using the Sharpened Cosine Similarity metric.

**Day 27-28:** Prepare documentation including model architecture, dataset creation, preprocessing steps, and evaluation results.

**Day 29:** Set up deployment infrastructure. Containerize the model using Docker if necessary.

**Day 30:** Deploy the model to a cloud platform or server. Test the deployed model with sample inputs.
