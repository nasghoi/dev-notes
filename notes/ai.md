# AI course

## Getting started
### Natural vs Artificial Intelligence
- **natural** - learning but take a lot of time
- we are tool builders
- computer scientist create ai
### History
1. 1950
- can machines think?
- **Turing Test** -> imitation game, is a test of a machine's ability to exhibit intelligent behavior equivalent to, or indistinguishable from, that of a human
2. 1956
- artificial intelligence terms start use
- explore if machines could stimulate variouus aspects of human intelligence
3. 1960s - 1970s
- known as **AI winter**
- technology and data availability limitation -> *reduced fundings and interest in AI research*
4. 1997
- **IBM Deep Blue** defeated world chess champion (Garry Kasparov)
- AI start gain attention
5. 1990s - 2000s
- known as **Advancement of Technology**
- Internet start growing up
6. 2006
- **Deep learning** have been explored by Geoffrey Hinton
- inspired by how the human brai works
7. 2011
- **IBM's Watson AI** won the "Jeorpardy!" quiz show
- showcase advances in NLP
8. 2012
- **Deep Neural Networks** article published by Jeff Dean and Andrew Ng
9. 2017
- **Google Brain** - huge breakthrough in NLP by introducing *transformer*
- allow to process text efficiently
10. 2018
- **OpenAI** released *GPT1*
- generative AI technology utilized `Transformer`to build **LLM**
11. Late 2022
- **ChatGPT** released

### AI vs Data Science vs Machine Learning
![ai-ds-ml](/images/ai-ds-ml.png)  
- **AI** claims to make machine intelligence, learn new skills
- **Machine learning** is AI key subfields - predict outcome
- **Data Science** work with ML - but, DS often use statistical method, rely on math, statistics and data visual

### Weak vs Strong AI
- **Narrow AI** - a machine that is able to perform specific task that it's been designed to do
- Semi-strong AI -> ChatGPT 3.5 (2022)
- Artifical General Intelligence (AGI) - Strong AI
- **AGI** should be able to create science on its own

## Data is essential for building AI
### Structured vs Unstructured Data  
1. **Structured Data** -> organize into row and columns (considered more valuable)
2. **Unstructured Data** -> text files, images, videos (lacks defined structure, but VALUABLE INSIGHTS $$$)
### How data have been collected  
![mnist](/images/mnist.png)  
- **MNIST Database** -> basic for student who want to learn ML (70k, 28 x 28 pixel images of handwritten digits)
- computer use ```binary form (0s & 1s)``` to store and process the data
- computer is trained to recognize numerical sequences
- AI get all the data by *scraping the web, accessing APIs and harnessing big data analytics*  
```Garbage DATA IN, Garbage DATA OUT```  
```Great DATA IN, Great MODEL OUTPUT```
### Labelled and Unlabelled data
1. **Labelled Data**
![labelled-data](/images/labelled-data.png)  
- reviews each photo and classifying the image
- also works with text, audio, video and other data types
- more reliable but time consuming and expensive
2. **Unlabelled Data**
![unlabelled-data](/images/unlabelled-data.gif)  
- quicker and cheaper
- ml advancements now allow us to work with UNSTRUCTURED data
- need to train the AI model
### Metadata: Data that describes data
- much of nowadays data is unstructured and too voluminous to label
- metadata **proves invaluable** here
1. **Metadata** -> Data that describes other data
```Your data should have metadata```
- Type of asset
- Author
- Date created
- Usage
- File size, etc.  

## Key AI techniques
### Machine learning
- similar to a student (ml model) taught by a teacher (data scientist)
- teacher help the student learn *how to solve the problems*
- ml algorithm learns to *recognize patterns*
- **Goal**: solve problems with *new* data  
```More UP TO DATE the data, the BETTER the model can solve NEW challenging problems```  
```
F(x) = y
Y = future price of home
x = property characteristics
```
### Supervised, Unsupervised & Reinforcement learning
1. Supervised Learning  
- work with *labelled data*
- solve *classification* problems
- make prediction (calculation) - **regression problem**
2. Unsupervised Learning  
- work with *unlabelled data*
- ml model will *scan through* all the data, look for **patterns**
- the model *can't specify* the data, but it just indicates the *similar characteristics* of each data
- labelling data is *costly*
3. Reinforcement Learning
- model can *decide* how to achieve the goal
- shares the understanding of *Supervised and Unsupervised learning*
- learns from interactions with the environment
- model learn from **try and error**, within specific parameters of it's **created rules**
- eg. robotics and online recommendation systems (Netflix)

### Deep Learning
![deep-learning](/images/deep-learning.png)  
1. Neural networks
![neural-networks](/images/neural-networks.gif)  
- **input layer** 
    - input info (raw images etc.)
    - *receives raw data*
    - simlar to senses sending info to brain
- **intermediate/hidden layer**
    - recognize complex features (shapes, specific objects)
    - *process input information*
    - neural can have *one or more* hidden layer
    - more layer, more learning capacity (needs to manage carefully)
- **output layer**
    - represent more complex aspects (final conclusion)
    - *generates final results*
![nn-layer](/images/nn-layer.png)  
> why do we need several layers  
- need to identify the *edges, curves, loops and intersections* of the data
- each layer need to learn *each part* of the data (top, bottom etc.)
- output layer *determine* either the data is true (recognize the digit is 3)

## Important AI branches
### Robotics
- branch of tech that deals with the design, construction, operation and use of robots
- people have been fascinated with robot for a long time
1. who's **involved**?
    - mechanical engineers - construct robots physical structures
    - electronic & electric engineers - design systems that enable the robot to operate 
2. Robots 
- various types of AI *drive the robot's* decision making and behaviour
- equipped with *various of sensors and cameras* to collect data and surroundings
- designed to *mimic* and *augment human abilities*
- have *multiple* types of AI
    - **computer vision** (object detection and environment understanding)
    - **navigation** (localization and mapping)
    - **reinforcement learning** (decision making)
    - **NLP** (understanding and generating human language)
- so, the robots can
    - perceive env
    - make decision
    - comm with people
    - act accordingly  
```Robotics Innovations Becoming Mainstream```
### Computer vision
- AI field that *uses ML and NN* to teach computers
- computers consume input *through images and videos*
1. Convolutional Neural Network (CNNs)
- great at *organizing the elements in an image* (based on importance and depth)
- great when working with *high-dimensional data*
- great capturing *spatial hierarchies in images*
- effective at processing information *due to layered structure*
2. Transformers
- AI researcher apply transformers archictecture to images for purposes of CV
3. Generative Adversarial Networks (GANs)
- Primarily create lifelike images
4. U-Net
- optimize performance by scaling NN dimensions & utilizing computational resources
> COMPUTER VISION does not need to be part of ROBOTICS to be an incredibly USEFUL product
- eg. face recognition software
### Traditional ML
- Generates *more significant portion* of business value
- Many type of industries have been used ML for the *over a decade and still increasing*
    - **finance institutions** - detect fraudulent and predict a customer's likelihood of repay mortgage
    - **insurance companies** - offer more precise pricing insurance packages
    - **retail companies** - predict demand and optimize orders
    - etc.
> TRADITIONAL AI continues to deliver significant value
### Generative AI
- create *new and unique data* or content
- producing *novel content by leveraging patterns* learned from training data
- Techniques to achieve Generative AI
1. LLMs
    - foundation behind ChatGPT
    - trained on vast text volumes
2. Diffusion Models
    - generate random noise -> refine images -> obtain realistic picture
3. GANs  
    ![gans](/images/gans.png)  
    - one generates content, other judges its realism
    - *Generator* creates images, *Discriminator* judges them
4. Neural Radiance Fields
    - specialized AI for 3D Modelling
5. Hybrid Models
    - LLMs + GANs - powerful *content-generation* systems
> GEN AI can create and work with: Text, images, videos, audio, data, code, design and 3D

## Understanding Generative AI
### Gen AI arisen: ChatGPT
- **ChatGPT 3.5** -> fine-tuned for dialogue (trained to produce text)
- AI tools that can
    - summarize text
    - respond to highly technical questions
    - assist any technical task
- **ChatGPT 4.0** -> showed tremendous leap

### Early approaches to NLP
- **NLP** - field of cs that studies *how computers understand, interpret and generate human language data* 
![rule-based](/images/rule-based.png)  
1. came around *1950s*, focused on *rule-based systems*
![statistical-nlp](/images/statistical-nlp.png)  
2. *1990s*, statistical NLP (capable to identify whether `can` is used as a *noun* or a *verb*)

### Recent NLP advancements
1. *2000s*, ML NLP (vector embeddings - transform words and sentences into numerical arrays)  
![vector-embed](/images/vector-embed.png)  
- each word in a setence can be represented as a vector
- stored in a high dimensional space called *vector embedding*
2. **Vector embedding dimension**  
![vector-embed-dimension](/images/vector-embed-dimension.png)  
- typically several hundred to thousands of dimensions deep
- not just 2 or 3 dimensions
- *human language* is complex (can't capture with 2/3 dimensions)
- use embeddings to store and retrieve data based on *semantic similarity*
3. *2010*  
![nn-2010](/images/nn-2010.png)  
- NN, with deep and multilayered structures (excel at detecting complex patterns)
4. *2018*  
![transformers-2018](/images/transformers-2018.png)  
- *Transformers* - it revolutionized the NLP field and *led to the creation of LLMs*

### LM to LLMs
- context is crucial
- LM are *probabilistic* (capable of predicting the missing words in a sentence, based on words before it)
-  TWO types of Language Model
1. *Masked* LM
- guess the missing words *regardless of its position* in a sentence
- use info before and after the blank space to fill the missing
2. *Autoregressive* LM
- *predict* the next word
- use *context of preceding words*
- eg. OpenAI's GPT model -> analyze and learn from the patterns & structures in the input text (digesting large data sets)
- generate an *infinite number* of possible outputs  
![gpt](/images/gpt.png)  
```LLM - trained on vast data quantities```  
```The RICHER the TRAINING DATA, the SMARTER and MORE VERSATILE they become```

### Efficiency of LLM training
1. Supervised Machine Learning
- *too expensive* - AI need to be trained using *labelled data*
- must pay the person to label the data
- LLM need *different* approach
2. Unsupervised Machine Learning
- *no goal* - operates without label
- not clear objective *without specific goal*
- language nuances *could be missed*
3. SOLUTION - Self-supervised Learning  
![self-supervised](/images/self-supervised.png)  
- the breakthrough, *led to the creation* of LMS
- it can :-
    - analyzes text datasets
    - generates labels
    - predicts content
    - use contextual cues from surrounding  
- this hybrid approach create *ChatGPT*

### The Evolution of NLP
```N-Grams -> RNNs -> Transformers```  
4 core Language Modelling techniques
1. N-grams
- estimate a word's probability based on the *preceding n-1 words*
- prediction is not based on any context
- n = 1 ('unigram') -> A *single* word
    - *would suggest common words*
    - Example:
    - Sentence: "I like eating rice"
    - Unigrams: ["I", "like", "eating", "rice"]
- n = 2 ('bigram') -> A pair of *two consecutive* words
    - *would suggest words that commonly follow others*
    - prediction depends solely on the previous one word
    - Example:
    - Sentence: "I like eating rice"
    - Bigrams: [("I", "like"), ("like", "eating"), ("eating", "rice")]
- n = 3 ('trigram') -> A pair of *three consecutive* words
    - *more context*
    - prediction based on the *last 2 words*
    - Example:
    - Sentence: "I like eating rice"
    - Trigrams: [("I", "like", "eating"), ("like", "eating", "rice")]
- predict based on *appearance frequencies* in the training data
2. Recurrent Neural Networks (RNNs)
- NN that works best with text
- retain info from prior steps
- analyze the *previous words* helps RNN network decide on the next word
    - order of words
    - context
- PROBLEM - *Vanishing Gradient issue* (difficulty in handling large texts, lose earlier info)
- SOLUTION - AI scientist developed *Long Short-Term Memory (LTMs)*
3. Long Short-Term Memory (LTMs)
- improved traditional RNN by introduce a *Gate Architecture* to choose which info to `retain` and which to `discard`
- this will *keeps long term* info and *forgets irrelevant* data
- *significantly better* at tasks involving COMPLEX TEXT DATA
- BUT, the drawbacks is :-
    - High computational cost
    - Slow training speed on LARGE data sets
4. Transformers.. and the ATTENTION mechanism
![trans-attention](/images/trans-attention.png)  
- identify *keywords*, `focus more`, `lower computational costs` and `enhance scalability`
- *this achieved* by **assigning an attention score (n)** to each word in the input sequence
- words with *higher attention* scores are consider more significant
- this *enable* transformers *to handle long range* dependencies

### Phases in building LLMs  
![build-llm-phases](/images/build-llm-phases.png)  
- sometimes the phases could OVERLAP
1. Model Design
- AI strategists and Dev *selecting the NN architecture* to employ
- they need to decide
    - the *depth* of the model
    - the *number of layers* of in the NN
    - the *total parameters* it will contain  
> A model is only GOOD as the data USED to build it
2. Dataset Engineering
- involve *collection*, *cleansing* and *structuring* of training data for the model
- Two ways to *acquire* data to build an AI model
    - Scrape public data
    - Use proprietary data (ownership) - sendiri **only few company have enough data
> Bernard Marr - AI Strategist
>> The companies that own the most proprietary data will likely have a competitive advantage when building AI systems
- need to consider data ETHICS and data DIVERSITY
3. Pretraining
- involve training the model on *LARGE corpus of raw data*
- the model could provide *undesired output*
- it's all based on the data that the model consume
4. Preliminary Evaluation
- evaluate preliminary (coming before, temporary) performance
-  *gain an idea* of its capabilities
- once the *understand what needs to be improved*, they address these issues in the `Post-training phase`
5. Post-training
- consists of TWO steps
    - *Supervised finetuning* with high quality data
    - Refine the model by *providing human feedback*
6. Finetuning
- updates the *model weight*
- we can make the model *smaller and faster* (suited for specific task, less capable in general performance)
7. Final Testing & Evaluation (again)
- BUT, this time, much STRICTER and *put ourselves* in END USER shoes
- evaluate the model's
    - response
    - quality
    - accuracy
    - speed
    - ethical behavior (the crucial one)

### Prompt engineering vs Fine-tuning vs RAG - Techniques for AI optimization  
![pe-rag-ft](/images/pe-rag-ft.png)  
- all these three techniques *enchance LLM's response accuracy and effectiveness*
- PE and RAG are effective, but to make an LLM smarter or faster, we need to modify its weight.
1. Prompt engineering
-  explain to the model *how to behave*
-  *don't change* any weights or *add new* data
-  use *verbal instructions* (explaining desired output we want to obtain)
-  *easy* level
-  can consistently refine the prompts through *multiple iterations*
> the model does not change, it adapts based on the verbal instructions
2. Retrieval-augmented generation (RAG)
- expand context by *attaching a library*
- *don't change* any weights or *add new* data
- attach a database (library/expanded context)
- *medium* level
> model does not change
3. Fine-tuning
- need ADDITIONAL training for an *already* trained model (pre-trained)
- extra data is REQUIRED to conduct fine-tuning
- weight *change* and *extra* data
- *hard* level
> model changes, can be computationally expensive and can't use an iterative process  
>> Assign it to new weights make it LIGHTER and FASTER to give responses QUICKER

### Importance of foundation models
- image recognition - identify objects within images
- speech recognition - spoken language to written text
- NLP models - sentiment analysis; translation
- time series - stock prices, market volatility
- `LLM` - excel in *general-purpose* tasks
- they can *perform well* in many field - lagi lagi kalau dah fine tuning dengan prompt engineering
> FOUNDATION MODELS (large pre-trained models)
  - enormouse
  - general purpose
  - immensely powerful
>> From Language Model to Multi-Modal Systems REAL QUICK!

### BUY IT or MAKE IT: foundation models vs private models
- BUY (outsource) vs MAKE (retain internally)  
![buy-vs-make](/images/buy-vs-make.png)  
- most companies face a *critical choice* either to
  - build ON an EXISTING foundation model OR
  - develop their OWN VERSION from an open-source model
- lack the `expertise` and `resources` to train a custom model
- they must rely on organizations like OpenAI, that offer foundation model (GPT)
- `Model-as-a-Service (MaaS)` - don’t own or run the AI model yourself — just use it over the internet (usually via an API) and pay based on usage

## Practical challenges in Generative AI
### Inconsistency and hallucination  
![rule-of-thumb](/images/rule-of-thumb.png)  
- BIG mistakes can occur if we don't FACT-CHECK
- TWO types of undesired behavior from Gen AI
    1. Hallucinations - provides *false output* to generate any production
       1. AI could be trained on factually *incorrect data*
       2. LEGIT TACTIC to deal with hallucinations - give instruction "Provide an answer *only if you know the answer*" 
    2. Inconsistencies - provides *very different responses* to the same question
       1. UNPROVEN WAY to reduce inconsistencies - instructing the AI to take its time "Take your time"
### Budgeting and API costs
![gpt-4-cost](/images/gpt-4-cost.png)  
- TWO main factors to determine how powerful (`MODEL PERFORMANCE`) an AI model is - 
  - Dataset size - enhances model learning capacity
  - Model size - determines learning capacity
> Larger AI model that has MORE parameters will be able to capture MORE detailed patterns
>> The LARGER an AI's *data set* and *model size*, the HIGHER its *performance* can be expected.
- consider plan AVAILABLE BUDGET beforehand and decide what PORTION will be allocated to `data acquisition` and `computing power`
1. **Large model** - more *computing power*, more expensive BUT boost in *effectiveness*
2. **Small model** - cost-*effective*, *quicker* to train (can be retrained and fine-tuned frequently)
### Latency
- today's user have LOW TOLERANCE for *slow loading times*
- LATENCY issue become MORE CRITICAL when business customers want to use AI to
  - boost personal productivity
  - build products based on an AI model
- the BIGGEST challenge of LLMs today is the models use an `Autoregressive Architecture`
> Autoregressive Architecture (synchronous)
>> where each word *generated depends on* the words that came *before it*
- EFFECTIVE immediate strategy is to optimize model size
- `Smaller` model FASTER than `larger` and `more complex` counterparts
### Running out of data  
- GPT-4 has already read *most of the internet’s public data*
- This raises the question: Where will *GPT-5 get new data?*
- AI developers might *run out of fresh, high-quality data*
- A lot of new online content *is now written by AI* (like ChatGPT)
- This means future AIs might `just read and learn from AI-generated content, not humans`
- As a result, future models could:
    - *Struggle to learn* new or deep ideas
    - *Keep seeing the same ideas* repeated
    - *Risk producing more* hallucinations, bias, or inaccuracies
1. Why Data Access is a Challenge for AI (Gen AI)
- Many large companies have *blocked data scraping* due to the rise of generative AI.
- Some have even *filed lawsuits*, including:
  - The New York Times  
  - Shutterstock  
  - John Grisham (bestselling author)
- Platforms like *Reddit* and *Quora* changed their policies to prevent AI developers from scraping data
2. How OpenAI is Solving It
- OpenAI started a *content licensing program* to legally access data
- They have already *signed agreements* with major content owners
3. Licensing Details
- OpenAI pays between *$1 million and $5 million per year* to access content
- These deals allow OpenAI to train its models on *high-quality, proprietary data*
4. Partners (So Far)
- Shutterstock  
- Axel Springer  
- The Associated Press  
- Le Monde  
- Prisa Media (future deal)
5. Rising Cost of Data for LLMs
- Big tech companies are *competing* to build better large language models (LLMs)
- This competition is likely to *drive up the prices* of large, *proprietary datasets*
- Owning high-quality data is becoming *more valuable* than ever

## AI Tech Stack
### Python programming
- *no code / low code* are popular way to get started with AI
- can use to develop *chatbots* and gain an idea how you can build your *own AI*
- also allow you to build *real life products*
- learn code is essential because its *allows you to use APIs*
- also enable you to *tailor AI behavior* (prompt engineering, integrate database & modify model parameters)
1. Python
- *leading* programming language for `data science` and `AI`
- it have
  - comprehensive *libraries* (numpy, pandas, matplotlib, tensorflow, pytorch)
    - **numpy** - multi-dimensional arrays, matrices and math functions
    - **pandas** - data preprocessing
    - **matplotlib** - data visualization
  - robust infrastructure
- Python IDEs (Jupyter Notebook, PyCharm, Spyder, Google Colab)

### Working with APIs
- use API to *facilitate data extraction*
- serves as BRIDGE between a client and a server, to communicate
- clients *sends a request* accross the bridge, and the server *responds with required data*
- the process involves TWO main steps
1. **The API Request** - client sends a request to the server
2. **The API Response** - server processes the request and sends back the required data

### Vector databases
- relational database *perfect* for STRUCTURED data
- but they are not OPTIMAL when it comes to UNSTRUCTURED data (*text, images, audio, video*)
- where to convert multimedia into a format that *computer can understand* (vector embeddings)
- *Vector embeddings* - that stored and organized in a *vector database*  
![vector-db](/images/vector-db.png)   
- *Vector database*
  - have *array of numbers* clustered together based on their *similarity*
  - organized based on similarity metrics (measure how *close or distant* are from each other)
  - we can have *millions of vector embeddings* but querying them would very SLOW *to ensure fast retrieval* of the data 
  - so, VDB rely on indexing and *use ML techniques* that allow them to search effieciently
  - VDBs giving LLMs LONG-TERM memory, by storing *past interactions/learned information* as vectors
  - so, the model can *reference past interactions* the data to *better understand* the context
  - eg. *Pinecone* (closed source), *Weaviate*, *Milvus*, *Elasticsearch* and *ChromaDB*

### Importance of Open source
- accelerated innovation (ability to rely on collective knowledge and creativity)
- critical factors that *boosted the growth of open source AI* is the users could *reduce hardware requirements* for AI development
- it will *snowballs* the innovation and model improvement
- proprietary models (like OpenAI's GPT) sense a threat because they have invested heavily in AI models, aim for significant returns
- ![open-vs-closed](/images/open-vs-closed-source.png)
- *Open source* (Weaviate, Milvus, ChromaDB) - *avoid* Google or OpenAI *fees* but incur *computing costs*
- *Closed source* (Gemini. Pinecone)
  - *easier* to implement
  - *offers plug-and-play* convenience with *minimal* configuration
  - your business data should have LOWER CHANCE of *leaking to the public*
![llama-meta](/images/llama-meta.png)
- In 2023, Meta’s LLaMA AI model `was leaked` (possibly not by accident)
- The leak ended up being *beneficial*
- The *open source community* started building tools and infrastructure on top of it
- This unexpectedly *helped Meta* improve its AI ecosystem.
- Meta combined:
  - Its *large resources* and investments
  - With the *power of community development*
- This shows a big tech company *benefiting from an open source approach*.
- Open source models will be advantageous for *narrow use cases* requiring a specialized AI
- Fine-tuning a CLOSED-source model can be *expensive* because some companies *charge significantly*
- Closed-source is more powerful when faced with complex tasks that require *generalized understanding and skills*
![big-tech-money](/images/big-tech-money.png)
- Big tech companies have the *money and resources* to buy *proprietary data*
- This gives them access to *high-quality, exclusive information*
- As a result, they can train *stronger foundation models*
- This widens the *performance gap* between them and smaller competitors

### Hugging Face (founded in 2016)
- like *Github* for machine learning and AI, because it aims to promote open source ML and AI
- leading *advocate* for Open source AI
- to train NLP transformer models, we need to *invest significant funds* (not feasible for startups and small businesses)
- HF giving everyone *access to pre-trained models*
- such models are *freely available* and can be used to *develop proprietary AI*
- HF introduced the *Transformers Python library* where it allows AI developers to *access pre-trained models via an API*
- this library provides an *efficient way* to create machine learning pipelines
- with HF, user can :-
  - share ML models
  - use pre-trained models
  - fine-tune models
  - host demos
  - evaluate ML models
- HF now boasts a valuation *exceeding $4.5 billion*, indicating substantial resources and commercial status
> HF infrastructure IS NOT open source; USER-UPLOADED models are

### LangChain
- open source *orchestration environment* available in Python and JavaScript
- LangChain’s *MODULAR components* let you swap foundation models easily without rewriting code — thanks to its *structured functions and classes*
- LC enables developers *to integrate multiple* foundation models and external data sources
- serves as LIBRARY, offering a collection of *commonly used* programming components and patterns
- designed to make it *easier and faster* for developers to build with language models by *simplifying complex tasks*
#### Without LangChain
![without-langchain](/images/without-langchain.png)
#### With LangChain
- LC lets you leverage *pre-built components* to build chatbots
- utilize components to handle :-
  - API interactions
  - data preprocessing
  - response generation
- can manage the entire workflow from *understanding the question* to *fetching* and *formatting* the appropriate answer
- these tools let developers *easily* and *quickly* integrate LLMs into their apps with a *user-friendly approach*
- allows for *less customization* than writing all LLM integrations *manually*
-  adding *long-term memory* (Chatbots, Virtual Assistants, Customer Support Systems)

### AI evaluation tools
- The hardest part wasn’t setting up the database
- It also wasn’t preparing interview questions or developer tasks
- The real challenge was:
  - *Prompt engineering* – designing effective prompts for the AI
  - *Shaping AI responses* – making sure the AI answers clearly and correctly
- This took the *most time and effort* in the development process
- After building an AI-powered product, *testing its output is crucial*
- Skipping this step can lead to:
  - *Hallucinations* (AI making things up)
  - *Inconsistent answers*
  - *Ethical problems* (biased or harmful output)
  - *Product issues* (like incorrect code generation)
- Today, *ethical issues are major deal-breakers* for users and companies
- Proper evaluation helps ensure the AI is *reliable, safe,* and *trustworthy* before going live
![ai-as-judge](/images/ai-as-judge.png)  
- A common method is to *use one AI to evaluate the output of another AI*
- This is known as the *"AI-as-a-judge"* approach
- It’s a fast and scalable way to *automate AI testing and feedback*  
![ai-as-a-judge-pros](/images/ai-as-a-judge-pros.png)  
![ai-as-a-judge-cons](/images/ai-as-a-judge-cons.png)  
- So, it's important to *involve human judges* in the evaluation process.

## AI job positions
### AI strategist  
![ai-strategist](/images/ai-strategist.png)  
- focusing on the *overall business strategy* and company goals from the outset
- identifying and suggesting *viable AI use cases*
- needs to be able to help their company *execute in practice*
- needs to envision *how the AI model will be deployed in production*
- and integrated into the firm's *existing* products
- set *procedures* to help the company evaluate
- optimize the *performance* of the AI models it has deployed
- AI evangelism
  - *promoting* AI adoption across the company
  - ensuring employees *understand* how AI can help the business become *more competitive*
- typically, *data scientists* are suitable for this role
- hired as *directors* or *heads* of a dedicated team as VP roles (C-suite roles)
> A GOOD data strategist knows what it takes to build a technical solution and has the business acumen to envision the project's impact
### AI developer  
![ai-developer](/images/ai-developer.png)  
- builds *foundation AI models*
- need to spend a *significant portion* of their time researching
- trying to *study ways to push the boundaries* of what AI can achieve
- R&D component of this role is essential
- it allows AI developers to stay abreast of industry developments and test new ideas
- research helps AI developers understand the optimal architecture for the solution
- *decide on the model design* to be used
- they need *strong knowledge* of NLP in semantic similarity, transformers, vector embeddings, tokenization and many others
- need *proficiency* in containerization, DevOps practices, and the ability to work with tools like Docker
### AI engineer  
![ai-engineer](/images/ai-engineer.png)  
- builds applications *on top of foundation* models
- 
- 
