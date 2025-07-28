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
- 



