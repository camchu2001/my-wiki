> **Resource**
> - [AI For Everyone](https://www.deeplearning.ai/courses/ai-for-everyone/)

According to a study by McKinsey Global Institute, AI would create an additional 13 to $22 trillion of value annually by 2033. 
* Of this 13 to 22 trillion to $4,000,000,000,000 is predicted to come from generative AI.
* The larger portion of the value is predicted to be from other forms of AI, e.g. supervised learning technology. 

AI is already creating **tremendous amounts of value in the software industry**. The McKinsey study points out that a lot of the value in the future lies outside the software industry, e.g. *retail, travel, transportation, automotive materials manufacturing, etc*. 
## I. Categories of Artificial Intelligence
1. **ANI (artificial narrow intelligence):** AIs that are designed and trained to perform **one specific** task or set of tasks proficiently (narrow task) but **lack general intelligence or self-awareness**. e.g. smart speakers, self-driving cars, image recognition, etc. 
2. **Generative AI:** an AI technology that can produce high-quality content, such as text, images, audio, or code. Generative models learn patterns in input data (training data) and generate new, similar data. e.g. ChatGPT, Bard, Midjourney, DAL-E. 
	* This is a bit *more general purpose*. Chat GPT can be a copy editor, brainstorming partner, text summarizer, etc. 
3. **AGI (artificial general intelligence):** a ***hypothetical*** AI system that could **perform any intellectual tasks that a human can**, and maybe more.
	* AI research is taking small steps to achieve AGI, but realistically, we are still very far from AGI. No AGI system exists yet. it may take many technological breakthroughs before we get there. 

> The rapid progress in ANI and generative AI has caused people to conclude that there’s a lot of progress in AGI, which leads to overblown and unnecessary fears about sentient robots taking over humanity. 

## II. Machine Learning
### 1. Supervised Learning
**Supervised learning** is the most commonly used type of machine learning. In supervised learning, the model is trained on a **labeled** dataset, where the **inputs are mapped to known outputs**. The goal is to develop a model capable of making accurate predictions on new input data, based on the patterns learned from the labeled training set.

<u>**Example:**</u> In spam detection (A = email, B = spam/not spam), the algorithms learn to <u>classify emails (A</u>) as <u>spam or not spam (B)</u> based on many examples of emails labeled as spam or not spam.

![](https://i.imgur.com/wynAFMj.png)

Supervised learning also lies at the heart of generative AI systems. These systems learn from huge amounts of text so that given a few words as the input, the models can predict the next word that comes after → **Large Language Models (LLM)**. LLM generates new texts by repeatedly predicting what is the next word they should output. 
#### Large Language Models (LLM)
Large language models are built by using supervised learning to **train a model to repeatedly predict the next word.** For example, the AI model is exposed to a massive corpus of text data from the internet, books, etc. This could include a sentence like *” My favorite drink is lychee bubble tea.”* This single sentence would be turned into a lot of A to B data points (input-output pairs) for the model to learn to predict the <u>next word (B)</u> given a few words as <u>input (A)</u>. 

![](https://i.imgur.com/8aPM9sy.png)

When we train a very large AI system on a lot of data (hundreds of billions of words), we get a Large Language Model like ChatGPT that given an initial text (prompt), is very good at generating additional words in response to that prompt. By training on a diverse corpus, it picks up on language patterns, grammar, semantics, and how words are statistically likely to follow one another in context.
* There are some more technical details behind how the model learns to follow instructions rather than just predict. 
* Developers also make the model less likely to generate inappropriate outputs, e.g. discrimination, harmful instructions, etc. 
#### Why is Supervised Learning taking off now?
For a **traditional AI**, as you feed it more data, its performance gets a bit better. But beyond a certain point, it did not get that much better. 
* e.g. a speech recognition system did not get that much more accurate, or an online advertising system didn't get that much more accurate at showing the most relevant ads even as you gave it more data.

But with modern AI, like deep neural networks, can continue to benefit from larger and larger amounts of data. As you feed these models more data, their performance keeps improving for much longer compared to traditional approaches.
* For many important applications like speech recognition, online advertising, self-driving cars, etc., achieving very high accuracy is crucial. Deep learning models can reach those high-performance levels when trained on massive datasets.

![](https://i.imgur.com/Zf6arK8.png)

The figure indicates, that to hit a high level of performance, you need two things: 
* have a lot of data → big data
* the ability to train large, high-capacity neural network models. 

The rise of specialized hardware like GPUs has enabled training these large neural networks on massive datasets to get very good performance. This scalability - *increasing both the data and model sizes* - is what has powered the recent breakthroughs in areas like generative AI and large language models (LLMs).