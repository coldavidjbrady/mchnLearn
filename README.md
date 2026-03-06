# IBM AI Engineering Professional Certificate (Coursera)

This repository contains my coursework, labs, and projects for **13 Coursera courses** that together make up the **IBM AI Engineering Professional Certificate**. Content is organized by course in the numbered folders at the project root (e.g., `Course 1 (ML w Python)`).

## Certificate overview

The IBM AI Engineering Professional Certificate is a hands-on curriculum focused on building practical, job-ready skills across:

- **Classical machine learning** (supervised + unsupervised learning, model evaluation, feature engineering)
- **Deep learning** foundations and implementation in **Keras/TensorFlow** and **PyTorch**
- Modern **Generative AI / LLM** concepts including **tokenization**, **transformers**, and **fine-tuning**
- Building **RAG (Retrieval-Augmented Generation)** pipelines and **agent-style** workflows (including LangChain-based patterns)

The end goal is to develop the ability to design, train, evaluate, and deploy ML/DL solutions—progressing from fundamentals to applied generative AI and retrieval systems.

## Repository structure

- `Course 1 (ML w Python)` … `Course 13 (Gen AI - RAG & LangChain)` — course-by-course labs and assignments
- `requirements.txt` — a pinned environment that works for the later courses in this repo (see notes below)

## Getting started (local setup)

### Prerequisites

- `git`
- **Python 3.11**
- A virtual environment tool (`venv`, `virtualenv`, `conda`, etc.)

### Clone the repo

```bash
git clone <YOUR_REPO_URL>
cd Coursera1
```

### Create and activate a virtual environment (recommended)

```bash
python3.11 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
```

### Install dependencies

```bash
python -m pip install -r requirements.txt
```

### Launch notebooks

```bash
jupyter lab
# or
jupyter notebook
```

## Dependency notes (important)

This repo spans multiple frameworks and eras of the Python ML ecosystem. In particular, **PyTorch**, **TensorFlow**, and **Keras** can have version constraints that conflict depending on the course/lab.

- The root `requirements.txt` is generated from the **current working virtual environment** used for the **later courses** in this repository.
- Some earlier course notebooks may require **different versions** (or different install approaches), especially around TensorFlow/Keras compatibility.
- If I were starting over, I would maintain **one virtual environment per course/project** (e.g., `Course 3/.venv`, `Course 10/.venv`) to avoid cross-course dependency drift.

## Courses (purpose & objectives)

Below is a course-by-course summary based on the content in this repository.

### Course 1 — Machine Learning with Python (`Course 1 (ML w Python)`)

**Purpose:** Build a strong foundation in applied machine learning using Python, with hands-on practice across the most common supervised and unsupervised techniques.

**Objectives**
- Prepare tabular datasets for modeling (cleaning, transforms, train/test split).
- Train and evaluate **classification** models (Logistic Regression, SVM, decision-tree style workflows).
- Train and evaluate **regression** models and interpret performance metrics.
- Apply **clustering** (e.g., K-Means) for segmentation problems.
- Complete an end-to-end final assignment integrating model selection and evaluation.

**Key artifacts in this repo**
- `Classification.ipynb`, `LogisticRegression.ipynb`, `SVM-cancer.ipynb`
- `K-MeansCluster.ipynb`, `CustomerSegmentation.csv`, `ChurnData.csv`
- `ML_FinalAssignment.ipynb`

### Course 2 — Deep Learning & Neural Networks with Keras (`Course 2 (Deep Learning w Keras)`)

**Purpose:** Learn core neural network concepts and implement practical models in **Keras**, progressing from fundamentals (forward propagation) to common applied architectures.

**Objectives**
- Understand forward propagation and core ANN building blocks.
- Implement regression workflows in Keras and evaluate results.
- Build and train **CNNs** for image-like data.
- Practice data handling and model iteration in notebook-driven workflows.

**Key artifacts in this repo**
- `ForwardPropgation.ipynb`, `KerasRegression.ipynb`, `KerasRegressionAssignment.ipynb`
- `CNN_with_Keras.ipynb`

### Course 3 — Deep Learning with Keras & TensorFlow (`Course 3 (DL with Keras and Tensorflow)`)

**Purpose:** Go beyond “basic Keras” into more advanced deep learning patterns using the Keras/TensorFlow stack (customization, generative models, RL-style labs, and modern architectures).

**Objectives**
- Apply **data augmentation** and **transfer learning** for image classification.
- Build **custom layers/models** and implement **custom training loops**.
- Implement representation learning approaches such as **autoencoders**.
- Explore generative modeling patterns (e.g., **GAN**-style workflows and diffusion-oriented labs).
- Work with transformer-based components and more advanced model configurations.

**Key artifacts in this repo**
- `DataAugmentationWithKeras.ipynb`, `ClassifyWasteProductsUsingTL.ipynb`
- `Custom_Layers_and_Models.ipynb`, `CustomTrainingLoopInKeras.ipynb`
- `BuildingAutoencoders.ipynb`, `DevelopGANsUsingKeras.ipynb`, `ImplementingDiffusionModels.ipynb`
- `AdvancedTransformers.ipynb`

### Course 4 — Introduction to PyTorch (`Course 4 (Intro PyTorch)`)

**Purpose:** Learn the PyTorch ecosystem and the fundamentals required to build, train, and evaluate models using tensors, datasets, and training loops.

**Objectives**
- Work fluently with **tensors**, broadcasting, and basic tensor math.
- Build **linear** and **logistic regression** models in PyTorch.
- Use dataset and transform utilities for image/text pipelines.
- Implement training/evaluation loops and understand optimization basics.

**Key artifacts in this repo**
- `2D_Tensors.ipynb`, `Image_DataSets_Transforms.ipynb`
- `LinearRegression1D.ipynb`, `LogisticRegression_5-1.ipynb`
- `BreastCancerClassification_6-1.ipynb`

### Course 5 — Deep Learning with PyTorch (`Course 5 (Deep Learning with PyTorch)`)

**Purpose:** Build deeper competence in PyTorch by implementing modern deep learning architectures and training techniques, especially for computer vision.

**Objectives**
- Implement and train **deep neural networks** using `torch.nn` modules.
- Understand and apply **activation functions**, **pooling**, and **normalization**.
- Build and train **convolutional neural networks** for image classification.
- Compare initialization strategies and measure training stability/performance.

**Key artifacts in this repo**
- `ActivationFunctions_5-3-5.ipynb`, `BatchNormalizationMNIST_5-4-9.ipynb`
- `ConvNeuralNetwork_5-5-6.ipynb`, `ConvNeuralNetSmallImages_5-5-5.ipynb`
- `ConvNeuralNetworkforAnimeImageClassification_5-6-1.ipynb`

### Course 6 — AI Deep Learning Capstone (`Course 6 (AI DL Capstone)`)

**Purpose:** Deliver an end-to-end capstone comparing and evaluating deep learning approaches across frameworks, with emphasis on experimentation, measurement, and reporting.

**Objectives**
- Implement consistent data-loading approaches in both Keras and PyTorch.
- Train comparable **Keras** and **PyTorch** classifiers on the same dataset(s).
- Compare performance via confusion matrices, ROC curves, and other metrics.
- Explore modern CV architectures such as **Vision Transformers (ViT)**.
- Integrate and evaluate multiple model components (e.g., CNN + ViT patterns).

**Key artifacts in this repo**
- `Keras-Based-Classifier_6-2-1.ipynb`, `PyTorch-Based-Classifier_6-2-2.ipynb`
- `Analysis-of-Keras-and-PyTorch-Models_6-2-3.ipynb`
- `Vision-Transformers-in-Keras_6-3-1.ipynb`, `Vision-Transformers-in-PyTorch_6-3-2.ipynb`
- `CNN-ViT-Integration-Evaluation_6-3-3.ipynb`

### Course 7 — Generative AI and LLMs (`Course 7 (Gen AI and LLMs)`)

**Purpose:** Introduce generative AI concepts and modern LLM tooling, with hands-on labs that cover key libraries and the text processing steps that power LLM applications.

**Objectives**
- Understand what makes a model “generative” and common use cases for GenAI.
- Work with tokenization and vocabularies as a bridge between text and tensors.
- Use modern libraries (e.g., Hugging Face Transformers) to interact with LLMs/chatbots.
- Prepare and load NLP-style datasets for model training and evaluation.

**Key artifacts in this repo**
- `Gen_AI_Libs.ipynb`, `Tokenization.ipynb`, `NLP_Data_Loader.ipynb`

### Course 8 — Generative AI Foundation Models for NLP (`Course 8 (Gen AI FMs for NLP)`)

**Purpose:** Build the NLP foundation needed to understand and use modern foundation models, including embeddings, language modeling, and sequence modeling patterns.

**Objectives**
- Implement or apply **word embeddings** (e.g., Word2Vec-style workflows).
- Build baseline language models (including n-gram/histogram approaches) to understand core concepts.
- Work with feed-forward and sequence modeling building blocks used in NLP systems.
- Train or apply transformer-family models for document tasks and language understanding.

**Key artifacts in this repo**
- `Word2Vec_8-2-1.ipynb`, `Word2Vec_8-2-2.ipynb`
- `LanguageModelling_8-1-2.ipynb`, `FeedForwardNeuralNetworks_8-1-3.ipynb`
- `ClassifyingDocument_8-1-1.ipynb`, `Sequence-to-Sequence_Model_8-2-2-3.ipynb`

### Course 9 — Generative AI Language Modeling with Transformers (`Course 9 (Gen AI Language Modeling with Transformers)`)

**Purpose:** Develop a working understanding of the transformer architecture and how it is applied to classification, translation, and language modeling.

**Objectives**
- Understand **self-attention** and **positional encoding**.
- Apply transformers for **text classification** tasks.
- Work with encoder/decoder patterns for translation-style problems.
- Understand data loading and text processing for BERT/transformer workflows.

**Key artifacts in this repo**
- `SelfAttn&PosEncoding_9-1-1.ipynb`, `ApplyingTransformersForClassification_9-1-2.ipynb`
- `DecoderCausalLangModels_9-2-1.ipynb`, `TransformersForTranslation_9-2-4.ipynb`
- `DataLoad_TextProc_BERT_9-2-3.ipynb`, `PreTrainingBERT_9-2-2.ipynb`

### Course 10 — Fine-Tuning Transformers (`Course 10 (Fine Tuning Transformers)`)

**Purpose:** Learn practical pre-training, inference, and fine-tuning workflows for transformer models using PyTorch and Hugging Face tooling.

**Objectives**
- Understand the difference between **pre-training** and **fine-tuning**.
- Run transformer inference and interpret outputs for downstream tasks.
- Fine-tune transformer models using Hugging Face training utilities and/or custom loops.
- Evaluate fine-tuned models and iterate on data/model settings.

**Key artifacts in this repo**
- `Pre-trainingLLMswithHuggingFace10-1-2.ipynb`
- `FineTuningTransformersWithHuggingFace_10-1-4.ipynb`
- `FineTuningTransformer-basedNNwithPytorch_10-1-3.ipynb`

### Course 11 — Fine-Tuning LLMs (`Course 11 (Fine-Tuning LLMs)`)

**Purpose:** Move beyond generic fine-tuning into instruction alignment and reward modeling concepts that underpin instruction-tuned models and preference-based training.

**Objectives**
- Perform **instruction tuning** using structured instruction/context/response data.
- Understand the role of alignment techniques (and where human feedback fits conceptually).
- Train/evaluate reward-model style workflows used in preference learning pipelines.

**Key artifacts in this repo**
- `Instructionfine-tuning_11-1-1.ipynb`
- `RewardTrainer_11-1-2.ipynb`

### Course 12 — Fundamentals of AI Agents: RAG & LangChain (`Course 12 (Fund of AI Agents - RAG & LangChain)`)

**Purpose:** Learn Retrieval-Augmented Generation (RAG) fundamentals by building retrieval + generation pipelines using Hugging Face/PyTorch patterns, including similarity search mechanics.

**Objectives**
- Understand the core RAG pipeline: **embed → retrieve → generate**.
- Build retrievers using transformer embeddings and evaluate similarity (cosine/dot product).
- Use FAISS-style vector search and compare “with vs without retrieval context”.
- Analyze embeddings and retrieval quality as a prerequisite to agentic workflows.

**Key artifacts in this repo**
- `RAGwithHuggingFace.ipynb`, `RAGwithPytorch-v1.ipynb`
- `prompt-engineering-v1.ipynb`, `companyPolicies.txt`
- `ReadMe_RAG.md` (notes comparing the two RAG labs)

### Course 13 — Generative AI: RAG & LangChain (`Course 13 (Gen AI - RAG & LangChain)`)

**Purpose:** Build applied, end-to-end RAG systems using **LangChain** patterns (loaders, splitters, vector stores, retrievers) and integrate with provider-backed LLM/embedding services.

**Objectives**
- Load documents from multiple sources using LangChain document loaders.
- Split text into chunks and generate embeddings for vector search.
- Configure a vector store and implement retrievers for semantic search.
- Build a **QA bot (RAG)** pipeline and evaluate answer quality.
- Integrate with IBM-flavored GenAI tooling in the LangChain ecosystem (where applicable).

**Key artifacts in this repo**
- `LangChain_Document_Loader_13-1-1.ipynb`, `LangChain_Text-Splitter_13-1-3.ipynb`
- `LangChain_Vector_Store_13-2-2.ipynb`, `LangChain_Retriever_13-2-3.ipynb`
- `QA_Bot_LangChain.ipynb`, `Embed_Docs__Watson_13-2-1.ipynb`
- `IBM_Cloud_Env.png`
