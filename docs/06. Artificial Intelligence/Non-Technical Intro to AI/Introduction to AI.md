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
### Supervised Learning
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
## III. Data
**Data** is usually presented as datasets (tables of data), or spreadsheets containing input features and output targets. It is up to the business use case to decide what constitutes the input features (A) and output targets (B) in the dataset. 

<u>**Example 1:**</u> Given the data set: 
* one might decide that the *size of the house and the number of bedrooms* is A and the *price of the house* is B, and have an AI system learn this input to output or A to B mapping.
* one might decide that input A is _the budget or amount someone wants to spend_, and output B is the _size of the house_ in square feet → the system can recommend the appropriate house size based on the provided budget.
![](https://i.imgur.com/zRNXOib.png)
### Acquiring Data 
#### 1. Manual Labeling
**Manual labeling** is the process of **manually annotating or labeling raw data** by human annotators or subject matter experts. 
* It involves going through individual data instances (such as images, text, or audio files) and assigning labels, categories, or annotations to them. 
* This method is particularly useful when *creating datasets for supervised machine learning tasks*, where labeled examples are required for training models.
#### 2. Observing Behaviors
**Observing behaviors** refers to the method of collecting data by observing and recording the interactions, actions, or behaviors of entities or systems.
* This can involve observing user behaviors on websites, applications, or platforms or observing the behavior of physical systems or machines. 
* This method allows for capturing real-world data without the need for manual labeling, and it is commonly used in applications like *recommendation systems, predictive maintenance, or user behavior analysis*.

<u>**Example 1**</u>: Consider an e-commerce or an electronic commerce website. One can observe if users buy their product or not and collect a dataset based on the users’ behavior. 
![](https://i.imgur.com/iImkfWD.png)

<u>**Example 2:** </u> If you run a large machine in a factory, and you want to predict if a machine is about to fail or has a fault, then just by observing the behavior of a machine, you can record a dataset. 
→ You can then define your *input features (A) as the machine ID, temperature, pressure, and other sensor readings*, and the *output target (B) as whether the machine failed or not*, allowing the system to predict potential failures based on the observed data.

![](https://i.imgur.com/HeAMumn.png)
#### 3. Download from websites/partnerships
- **Downloading from Websites**: involves accessing and downloading publicly available datasets from various websites or online repositories.
- **Obtaining Data from Partners**: involves acquiring data by collaborating or partnering with organizations or entities that have already collected relevant data. 
	- If you're building a predictive maintenance system for factory machines, you could partner with a factory that has already collected data on machine parameters (like temperature, and pressure) and failure events. Through this partnership, the factory can provide you with their existing dataset, which you can then use to train your predictive maintenance models.

> **Note**: When downloading datasets from websites or obtaining them from partners, it's crucial to respect licensing and copyright agreements