# How to use LLM to better solve CV tasks

## Image-Text basic model

- Image-Text Matching
- Image-Text Retrieval
- VQA
- Image-Caption



-----------------------------------
## Image Captioning
- [ChatGPT Asks, BLIP-2 Answers: Automatic Questioning Towards Enriched Visual Descriptions](https://arxiv.org/pdf/2303.06594.pdf)
    - VQA + ChatGPT
    -  Use BLIP-2 to generate caption first, design a prompt to instruct llm to ask high-quality questions based on the generated caption. use these questions and BLIP-2 to accomplish VQA task. Finally, use chatgpt to generate the new caption based on the VQA history.


**Idea:**

## VQA
- [From Images to Textual Prompts: Zero-shot Visual Question Answering with
Frozen Large Language Models](https://arxiv.org/pdf/2212.10846.pdf):
    - First use the question to cut the image into several patches, perform    Image-Question Matching to select related patches.
    - Generate image captions of related patches as question-related captions.
    - Extract keywords of the captions as answers, generate question-answer pairs according to the keywords and captions.
    - Cat related captions and QA-pairs together as LLM's input to generate answer.
    
    ![Img2LLM](assets/img1.png)

**Idea:**

## Visual Grounding 

- [ViperGPT: Visual Inference via Python Execution for Reasoning](https://arxiv.org/pdf/2303.08128.pdf)

    - Patch the image.
    - Using all the patches find the grounding object.
    - Sort the finding results.
    - Better than zero-shot (72 IoU), much lower than supervised models (94 IoU).

**Idea:**


## Segmentation 

- ????

## Image Expansion

- Dataset?





------------
## Related Paper
### [ViperGPT: Visual Inference via Python Execution for Reasoning](https://arxiv.org/pdf/2303.08128.pdf)
- Offer foundation models: (GLIP.find, GLIP.exists, X_VLM.verify_property ......).
- Create prompt including the description of the foundation models and task instructions.
- Using CodeX and the prompt to generate excutable code to solve the task.




