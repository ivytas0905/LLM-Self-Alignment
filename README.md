# LLM-Self-Alignment
The reproduce of the Self-Alignment Paper,Step1: Finetune the base language model (llama2 7B) with (output, instruction) pairs {(yi, xi)} from the seed data to obtain a backward model Myx := p(x|y). In other words, finetune a model that uses the output to predict the instruction. Use the openassistant-guanaco training set dataset.
step 2:Self-Augmentation -- Randomly sample a subset of size 150 and generate instructions from the LIMA dataset’s completions and filtering out any mutli-turn examples. Print out 5 examples of generated instructions. 
step 3:Self curation (selecting high quality examples) using few shot prompting in addition to the prompt in Table 1 of the paper. Print out 5 examples of high quality examples and 5 examples of low quality examples.
step 4:Finetune base model on dataset generated by step 3. Print out 5 example responses.
