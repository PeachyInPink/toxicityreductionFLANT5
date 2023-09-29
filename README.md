# This is Lab 3 of Generative AI with Large Language Models Course

### Executive Summary:
1. This project aimed to fine-tune a FLAN-T5 language model to reduce toxicity in generated summaries utilizing Meta AI's hate speech reward model.
2. Employed Proximal Policy Optimization (PPO) for fine-tuning to adapt the model in minimizing toxic content generation.
3. Integrated a pretrained RoBERTa-based hate speech model to serve as the reward model guiding the reinforcement learning (RL) process.
4. Utilized Hugging Face transformers and datasets, implementing in a PyTorch environment to conduct the fine-tuning.
5. Created a reward function based on the hate speech model's output, where higher rewards were allocated for less toxic text and lower rewards for more toxic content.
6. Prepared and processed the DialogSum dataset, focusing on dialogues of a particular length, to train and test the model.
7. During PPO training, only the parameters of the ValueHead were updated to optimize the RL policy against the reward model, minimizing deviation from the original language model.
8. Employed a toxicity evaluation metric to assess the model before and after detoxification, demonstrating a reduction in toxicity in generated summaries post-fine-tuning.
9. Compared toxicity scores before and after detoxification, establishing the effectiveness of the fine-tuning process in lowering toxicity.
10. Stored, reviewed, and sorted the results to analyze the difference in reward mean/median of generated sequences, evidencing a significant improvement.
