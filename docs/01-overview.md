# MedGemma

The MedGemma collection contains Google's most capable open models for medical text and image comprehension, built on Gemma 3. Developers can use MedGemma to accelerate building healthcare-based AI applications. MedGemma comes in two variants: a 4B multimodal version and a 27B text-only version.

For details about how to use the model and how it was trained, see the MedGemma model card.

## Common use cases
The following sections present some common use cases for the model. You're free to pursue any use case, as long as it adheres to the Health AI Developer Foundations terms of use.

### Medical image classification
MedGemma 4B's pre-training makes it a good starting point to be adapted for use in classifying medical images including radiology, digital pathology, fundus and skin images. MedGemma's baseline performance is strong compared to similar models of its size, but developers should validate its performance and make necessary improvements before deploying it in a production environment.

### Medical image interpretation
MedGemma 4B's pre-training makes it a good starting point to be adapted for use in generating medical image reports or answering natural language questions about medical images. MedGemma's baseline performance is strong compared to similar models of its size, but is not clinical grade, so additional fine-tuning is likely to be required.

### Medical text comprehension and clinical reasoning
MedGemma can be adapted for use cases that require medical knowledge. Such use cases may include patient interviewing, triaging, clinical decision support, and summarization. For most use cases, the larger MedGemma 27B model will generally yield the best performance. Both sizes of MedGemma have a strong baseline performance compared to similar models of their size, but developers should validate their adapted model's performance and make necessary improvements before deploying in a production environment.

## Adapting MedGemma
MedGemma is a developer model that requires validation on the developer's intended use case. Based on those validation results, the user will likely need to further adapt the model to improve performance. Below are some types of adaptation developers can use to improve MedGemma's performance for their use cases.

### Prompt engineering/in-context learning
For certain use cases, MedGemma's baseline performance may be sufficient after careful prompting, potentially including few-shot examples of desirable example responses within the prompt, in other words in-context learning. Prompt engineering may also use MedGemma to break the task into subtasks that can be performed separately. Adaptations using prompt engineering require the same level of validation as any other type of adaptation.

### Fine-tuning
MedGemma can be fine-tuned for improved performance on the existing tasks it's been trained on, or to add additional tasks to its repertoire. For an example of how to fine-tune MedGemma using LoRA (a parameter-efficient fine-tuning technique), see this notebook.

Users can specifically fine-tune the language model decoder component to help the model better interpret the visual tokens produced by the image encoder, or fine-tune both.

### Agentic orchestration
MedGemma can be used as a tool within an agentic system, coupled with other tools, like web search, FHIR generators/interpreters, Gemini Live for bidirectional audio conversation, or Gemini 2.5 Pro for function calling or reasoning. MedGemma can also be used to parse private health data locally before sending anonymized requests to centralized models like Gemini 2.5 Pro.

## Next steps

Get started using the model