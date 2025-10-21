\documentclass[11pt,a4paper]{report}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{geometry}
\usepackage{hyperref}
\usepackage{graphicx}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{enumitem}
\usepackage{xcolor}
\usepackage{tcolorbox}
\usepackage{tabularx}
\usepackage{booktabs}
\usepackage{fancyhdr}
\usepackage{titlesec}
\usepackage{parskip}

% Page setup
\geometry{
    top=25mm,
    bottom=25mm,
    left=25mm,
    right=25mm
}

% Color definitions
\definecolor{essential}{RGB}{220, 38, 127}
\definecolor{desirable}{RGB}{100, 143, 255}
\definecolor{highlight}{RGB}{254, 197, 21}
\definecolor{darkblue}{RGB}{0, 48, 135}

% Hyperref setup
\hypersetup{
    colorlinks=true,
    linkcolor=darkblue,
    filecolor=magenta,      
    urlcolor=blue,
    pdftitle={Comprehensive 2-Year Study Plan: Software Engineer to Applied AI/ML Research Engineer},
    pdfauthor={AI/ML Study Plan},
    bookmarks=true,
    bookmarksopen=true,
    bookmarksnumbered=true
}

% Custom commands for labels
\newcommand{\Essential}{\textcolor{essential}{\textbf{[E]}}}
\newcommand{\Desirable}{\textcolor{desirable}{\textbf{[D]}}}

% Title formatting
\titleformat{\chapter}[display]
{\normalfont\huge\bfseries\color{darkblue}}{\chaptertitlename\ \thechapter}{20pt}{\Huge}
\titleformat{\section}
{\normalfont\Large\bfseries\color{darkblue}}{\thesection}{1em}{}
\titleformat{\subsection}
{\normalfont\large\bfseries}{\thesubsection}{1em}{}

% Header and footer
\pagestyle{fancy}
\fancyhf{}
\rhead{\thepage}
\lhead{\leftmark}
\renewcommand{\headrulewidth}{0.4pt}

\begin{document}

\begin{titlepage}
    \centering
    \vspace*{2cm}
    
    {\Huge\bfseries Comprehensive 2-Year Study Plan\par}
    \vspace{1cm}
    {\LARGE From Software Engineer to\par}
    {\LARGE Applied AI/ML Research Engineer\par}
    \vspace{2cm}
    
    {\Large\itshape Enterprise-Level Career Transition Guide\par}
    \vspace{1.5cm}
    
    \begin{tcolorbox}[colback=blue!5!white,colframe=darkblue,title=Your Background]
    \begin{itemize}[leftmargin=*]
        \item 5 years of Computer Vision and Machine Learning experience
        \item Electronic Engineering degree
        \item Basic PyTorch and TensorFlow knowledge
        \item Focus: Applied Research for Production Systems
    \end{itemize}
    \end{tcolorbox}
    
    \vspace{1.5cm}
    
    {\Large Timeline: 24 Months\par}
    {\Large Investment: \$1,000-1,500\par}
    {\Large Time Commitment: 25-30 hours/week\par}
    
    \vfill
    
    {\large \today\par}
\end{titlepage}

\tableofcontents
\newpage

\chapter{Executive Overview}

\section{Market Demands and Career Path}

Applied Research Engineers at enterprise level represent a unique blend of skills: \textbf{60\% engineering, 40\% research}. Based on 2024-2025 job market analysis, top companies (Google, Meta, OpenAI, Anthropic, Microsoft) seek candidates who can implement cutting-edge research at scale.

\subsection{Key Industry Trends (2025)}
\begin{itemize}
    \item PyTorch dominates (42\% of job postings)
    \item AWS leads cloud platforms (35\% of roles)
    \item PhD preference growing (36.2\% of positions)
    \item Hot areas: LLMs/Generative AI, multi-modal models, MLOps maturity, on-device optimization
\end{itemize}

\subsection{Your Starting Advantages}
\begin{enumerate}
    \item 5 years Computer Vision experience
    \item Engineering degree foundation
    \item Basic PyTorch/TensorFlow knowledge
    \item Production mindset from software engineering
\end{enumerate}

\subsection{Critical Gaps to Fill}
\begin{enumerate}
    \item Deep learning theory and mathematical foundations
    \item Implementing models from scratch
    \item NLP and Reinforcement Learning domains
    \item Production ML infrastructure (MLOps)
    \item Research paper implementation skills
\end{enumerate}

\section{Study Plan Structure}

This plan is divided into 8 phases across 24 months:

\begin{table}[h!]
\centering
\begin{tabular}{|l|l|l|}
\hline
\textbf{Year} & \textbf{Phase} & \textbf{Focus Area} \\
\hline
\multirow{4}{*}{Year 1} & Phase 1 (Months 1-4) & Mathematical Foundations \& ML Basics \\
& Phase 2 (Months 5-8) & Deep Learning Foundations \\
& Phase 3 (Months 9-12) & Natural Language Processing \\
& Phase 4 (Month 12) & Year 1 Consolidation \\
\hline
\multirow{4}{*}{Year 2} & Phase 5 (Months 13-16) & Multi-Modal \& Modern Architectures \\
& Phase 6 (Months 17-18) & Deep RL \& RLHF \\
& Phase 7 (Months 19-21) & Production ML \& MLOps \\
& Phase 8 (Months 22-24) & Specialization \& Portfolio \\
\hline
\end{tabular}
\end{table}

\chapter{Year 1: Foundations to Applied Research}

\section{Phase 1: Mathematical Foundations \& Deep Learning Theory (Months 1-4)}

\subsection{Month 1-2: Mathematics Refresher \Essential}

\subsubsection{Core Textbook}
\textbf{Mathematics for Machine Learning} by Deisenroth, Faisal, Ong\\
Available free: \url{https://mml-book.github.io/}

\textbf{Essential Chapters (180 pages):}
\begin{itemize}
    \item \textbf{Chapter 2: Linear Algebra} (pp. 30-60) \Essential
    \begin{itemize}
        \item Matrices, eigenvalues, eigenvectors, SVD
        \item Review/skim familiar sections given your engineering background
    \end{itemize}
    \item \textbf{Chapter 3: Analytic Geometry} (pp. 60-80) \Essential
    \begin{itemize}
        \item Norms, inner products, orthogonality
    \end{itemize}
    \item \textbf{Chapter 4: Matrix Decompositions} (pp. 80-110) \Essential
    \begin{itemize}
        \item Critical: Eigendecomposition and SVD (pp. 95-110)
    \end{itemize}
    \item \textbf{Chapter 5: Vector Calculus} (pp. 110-145) \Essential
    \begin{itemize}
        \item Gradients, Jacobians, Hessians, chain rule
        \item Section 5.5: Gradients of vector-valued functions (CRITICAL for backprop)
    \end{itemize}
    \item \textbf{Chapter 6: Probability and Distributions} (pp. 145-180) \Essential
    \item \textbf{Chapter 7: Continuous Optimization} (pp. 180-220) \Essential
\end{itemize}

\subsubsection{Parallel Coursera Course}
\textbf{Mathematics for Machine Learning Specialization} (Imperial College London)
\begin{enumerate}
    \item Linear Algebra (5 modules, 2 weeks) \Essential
    \item Multivariate Calculus (6 modules, 2 weeks) \Essential
    \item PCA (4 modules, 2 weeks) \Desirable
\end{enumerate}

\begin{tcolorbox}[colback=yellow!10!white,colframe=yellow!50!black,title=Time Commitment]
\begin{itemize}
    \item 10 hours: Textbook reading + exercises
    \item 5-8 hours: Coursera lectures + assignments
    \item 2-5 hours: Implementation practice (NumPy from scratch)
    \item \textbf{Total: 15-20 hours/week}
\end{itemize}
\end{tcolorbox}

\subsubsection{Hands-On Project 1}
Implement Core Algorithms from Scratch:
\begin{itemize}
    \item Linear regression with gradient descent (NumPy only)
    \item Logistic regression with regularization
    \item PCA for dimensionality reduction
    \item Visualization of gradients and loss landscapes
\end{itemize}

\subsection{Month 3-4: Machine Learning Fundamentals \Essential}

\subsubsection{Coursera Course}
\textbf{Machine Learning Specialization} by Andrew Ng (Stanford/DeepLearning.AI)

\textbf{Course 1: Supervised ML - Regression and Classification} (~3 weeks) \Essential
\begin{itemize}
    \item Linear regression, logistic regression, gradient descent
    \item Overfitting, regularization (L1/L2)
    \item Python with NumPy \& scikit-learn
\end{itemize}

\textbf{Course 2: Advanced Learning Algorithms} (~4 weeks) \Essential
\begin{itemize}
    \item Neural networks fundamentals
    \item Decision trees, ensemble methods
    \item TensorFlow implementation
    \item Bias-variance tradeoff, model evaluation
\end{itemize}

\textbf{Course 3: Unsupervised Learning, Recommenders, RL} (~3 weeks) \Essential
\begin{itemize}
    \item Clustering, anomaly detection
    \item Recommender systems
    \item Introduction to RL (foundation for later)
\end{itemize}

\subsubsection{Textbook Reading}
\textbf{Deep Learning} by Goodfellow, Bengio, Courville\\
Free online: \url{https://www.deeplearningbook.org/}

\textbf{Essential Reading:}
\begin{itemize}
    \item Chapter 5: Machine Learning Basics (pp. 100-166) \Essential
    \begin{itemize}
        \item ALL sections essential
        \item Capacity, overfitting, underfitting, hyperparameters
        \item Maximum likelihood, Bayesian statistics
        \item Bias-variance decomposition
    \end{itemize}
\end{itemize}

\subsubsection{Hands-On Project 2}
Kaggle Competition (Tabular Data):
\begin{itemize}
    \item Choose beginner-friendly competition (Titanic, House Prices)
    \item Complete end-to-end ML pipeline
    \item Use scikit-learn, document workflow
\end{itemize}

\section{Phase 2: Deep Learning Foundations (Months 5-8)}

\subsection{Month 5-6: Neural Networks \& Backpropagation \Essential}

\subsubsection{Coursera Course}
\textbf{Deep Learning Specialization} by Andrew Ng (DeepLearning.AI)

\textbf{Course 1: Neural Networks and Deep Learning} (~4 weeks) \Essential
\begin{itemize}
    \item Forward propagation, activation functions
    \item \textbf{Backpropagation (CRITICAL)}
    \item Vectorization, gradient descent optimization
    \item Shallow vs deep networks
\end{itemize}

\textbf{Course 2: Improving Deep Neural Networks} (~3 weeks) \Essential
\begin{itemize}
    \item Optimization algorithms: SGD, momentum, RMSprop, Adam
    \item Regularization: L2, dropout, data augmentation, batch normalization
    \item Hyperparameter tuning: systematic approaches
    \item TensorFlow/Keras implementation
\end{itemize}

\subsubsection{Textbook Deep Dive}
\textbf{Deep Learning (Goodfellow) - Part II: Deep Networks}

\textbf{Chapter 6: Deep Feedforward Networks} (pp. 167-223) \Essential
\begin{itemize}
    \item ALL sections essential
    \item Section 6.5: Back-Propagation (pp. 200-220) - MUST MASTER
    \item Computational graphs, chain rule, automatic differentiation
\end{itemize}

\textbf{Chapter 7: Regularization} (pp. 224-270) \Essential
\begin{itemize}
    \item Essential: Sections 7.1, 7.4, 7.5, 7.8, 7.12
    \item L2/L1, dropout, early stopping, data augmentation
\end{itemize}

\textbf{Chapter 8: Optimization for Training} (pp. 271-325) \Essential
\begin{itemize}
    \item ALL sections essential for applied research
    \item SGD variants, momentum, Adam, RMSprop
    \item Section 8.5: Adaptive Learning Rates (pp. 302-307) - CRITICAL
    \item Batch normalization, gradient clipping
\end{itemize}

\begin{tcolorbox}[colback=red!10!white,colframe=red!50!black,title=Critical Requirement]
\textbf{Project 3: Neural Network Library in NumPy} \Essential\\
Build multilayer perceptron from scratch with:
\begin{itemize}
    \item Forward pass (matrix operations)
    \item Backpropagation (chain rule implementation)
    \item Multiple activation functions (ReLU, sigmoid, tanh)
    \item SGD, momentum, Adam optimizers
    \item L2 regularization, dropout
    \item Train on MNIST, achieve >95\% accuracy
\end{itemize}
\textbf{Goal: Deep understanding before using frameworks}
\end{tcolorbox}

\subsection{Month 7-8: Convolutional Networks \& Computer Vision Depth \Essential}

\subsubsection{Coursera Course}
\textbf{Course 4: Convolutional Neural Networks} (~4 weeks) \Essential
\begin{itemize}
    \item CNN architectures: LeNet, AlexNet, VGG, ResNet, Inception
    \item Object detection: YOLO, R-CNN family
    \item Transfer learning and fine-tuning
    \item MobileNet (efficient architectures)
\end{itemize}

\subsubsection{Advanced CV Resources}
\textbf{Computer Vision: Algorithms and Applications} (2nd Ed, 2022) by Richard Szeliski\\
Free online: \url{https://szeliski.org/Book/}

Essential Chapters:
\begin{itemize}
    \item Chapter 5: Deep Learning \Essential - NEW in 2nd edition
    \item Chapter 6: Image Features \& Alignment (pp. ~200-250) \Desirable
\end{itemize}

\subsubsection{Modern CV Architectures}
\textbf{Vision Transformers, CLIP, Diffusion Models} \Essential
\begin{itemize}
    \item Vision Transformer (ViT) implementation
    \item CLIP for multi-modal learning
    \item Latest object detection: YOLOv10/v11
\end{itemize}

\subsubsection{Hands-On Projects}
\textbf{Project 4: Advanced CV Implementation} \Essential\\
Choose one to implement from scratch:
\begin{itemize}
    \item ResNet on CIFAR-10/ImageNet
    \item Object Detection: Implement YOLO on custom dataset
    \item Segmentation: U-Net on medical imaging or COCO
\end{itemize}

\textbf{Project 5: Vision Transformers} \Essential
\begin{itemize}
    \item Implement ViT from "Attention Is All You Need" principles
    \item Fine-tune pre-trained ViT (Hugging Face Transformers)
    \item Compare with CNN performance
\end{itemize}

\section{Phase 3: Natural Language Processing (Months 9-12)}

\subsection{Month 9-10: NLP Fundamentals \& Transformers \Essential}

\subsubsection{Primary Textbook}
\textbf{Speech and Language Processing} (3rd Ed, 2025 Draft) by Jurafsky \& Martin\\
Free online: \url{https://web.stanford.edu/~jurafsky/slp3/}

Essential Chapters:
\begin{itemize}
    \item Chapter 2: Tokenization, Text Processing (pp. ~20-40) \Essential
    \item Chapter 6: Vector Semantics and Embeddings (pp. ~100-130) \Essential
    \item Chapter 7: Neural Networks (pp. ~130-160) \Essential
    \item \textbf{Chapter 9: Transformers} (pp. ~180-220) \Essential $\star$
    \begin{itemize}
        \item Self-attention, multi-head attention, positional encoding
        \item Architecture deep dive
    \end{itemize}
\end{itemize}

\subsubsection{Landmark Paper}
\textbf{"Attention Is All You Need"} (Vaswani et al., 2017) \Essential\\
arXiv: \url{https://arxiv.org/abs/1706.03762}\\
\textit{Cited 173,000+ times - Foundation of all modern NLP}

Read multiple times:
\begin{enumerate}
    \item First pass: High-level understanding
    \item Second pass: Implementation details
    \item Third pass: Mathematical derivations
\end{enumerate}

\subsubsection{Supplementary Resources}
\textbf{Natural Language Processing with Transformers} by Tunstall, von Werra, Wolf

Essential Chapters:
\begin{itemize}
    \item Chapter 1: Hello Transformers (pp. 1-30) \Essential
    \item Chapter 2: Text Classification (pp. 31-60) \Essential
    \item \textbf{Chapter 3: Transformer Anatomy} (pp. 61-100) \Essential $\star$
\end{itemize}

\begin{tcolorbox}[colback=blue!10!white,colframe=blue!50!black,title=Critical Implementation]
\textbf{Project 6: Transformer from Scratch} \Essential\\
Implement core transformer architecture in PyTorch:
\begin{itemize}
    \item Self-attention mechanism
    \item Multi-head attention
    \item Positional encoding
    \item Encoder-decoder architecture
    \item Train on machine translation task
\end{itemize}
\end{tcolorbox}

\subsection{Month 11-12: Large Language Models \& Modern NLP \Essential}

\subsubsection{Advanced NLP Topics}
\textbf{Speech and Language Processing} (continued)

Essential Chapters:
\begin{itemize}
    \item Chapter 10: Large Language Models (pp. ~220-260) \Essential $\star$
    \item Chapter 11: Masked Language Models (pp. ~260-290) \Essential
    \item Chapter 12: Alignment, Prompting, In-Context Learning (pp. ~290-330) \Essential $\star$
    \begin{itemize}
        \item DPO (Direct Preference Optimization)
        \item Prompt engineering, few-shot prompting
        \item Critical for 2025 roles
    \end{itemize}
\end{itemize}

\subsubsection{Key Papers to Read \Essential}
\begin{enumerate}
    \item \textbf{BERT} (Devlin et al., 2018)
    \item \textbf{GPT-1} (Radford et al., 2018)
    \item \textbf{GPT-3} (Brown et al., 2020)
    \item \textbf{InstructGPT} (Ouyang et al., 2022) - RLHF
    \item \textbf{Llama 3} (Meta, 2024)
\end{enumerate}

\subsubsection{Hands-On Projects}
\textbf{Project 8: LLM Fine-Tuning} \Essential
\begin{itemize}
    \item Fine-tune Llama 3 or similar open model
    \item Use Parameter-Efficient Fine-Tuning (LoRA/QLoRA)
    \item Tools: Hugging Face PEFT, bitsandbytes
\end{itemize}

\textbf{Project 9: RAG System} \Essential
\begin{itemize}
    \item Build Retrieval-Augmented Generation application
    \item Vector database (FAISS, Pinecone, or Weaviate)
    \item LangChain or LlamaIndex framework
    \item Deploy as web application
\end{itemize}

\section{Phase 4: Year 1 Consolidation (End of Month 12)}

\subsection{Year 1 Assessment Checklist}
\begin{itemize}
    \item[$\square$] Can implement neural networks from scratch (NumPy)
    \item[$\square$] Deep understanding of backpropagation and optimization
    \item[$\square$] Proficient with PyTorch/TensorFlow
    \item[$\square$] Implemented ResNet or similar CNN from scratch
    \item[$\square$] Implemented Transformer from scratch
    \item[$\square$] Fine-tuned BERT and GPT models
    \item[$\square$] Read and understood 5+ landmark papers
    \item[$\square$] Built 5+ complete projects with deployed demos
\end{itemize}

\subsection{Holiday Break Project}
Create GitHub portfolio showcasing:
\begin{itemize}
    \item All implementations from scratch
    \item Deployed projects (CV models, NLP applications)
    \item Blog posts explaining key concepts
    \item Code with documentation and tests
\end{itemize}

\chapter{Year 2: Advanced Domains \& Production Excellence}

\section{Phase 5: Multi-Modal \& Modern Architectures (Months 13-16)}

\subsection{Month 13-14: Vision Transformers \& Multi-Modal Models \Essential}

\subsubsection{Key Papers \Essential}
\begin{enumerate}
    \item \textbf{Vision Transformers (ViT)} - "An Image is Worth 16x16 Words"
    \item \textbf{CLIP} - "Learning Transferable Visual Models from Natural Language"
    \item \textbf{DINOv2} - "Learning Robust Visual Features without Supervision"
    \item \textbf{Diffusion Models} - DiffiT (ECCV 2024)
\end{enumerate}

\subsubsection{Hands-On Projects}
\textbf{Project 10: Multi-Modal Application} \Essential
\begin{itemize}
    \item Implement CLIP-based system
    \item Image-text retrieval
    \item Zero-shot image classification
    \item Visual question answering
    \item Deploy with Gradio/Streamlit
\end{itemize}

\textbf{Project 11: Segment Anything (SAM) Application} \Essential
\begin{itemize}
    \item Use Meta's SAM/SAM 2
    \item Promptable segmentation
    \item Video object tracking
    \item Integration with YOLO for detection + segmentation
\end{itemize}

\subsection{Month 15-16: Reinforcement Learning Foundations \Essential}

\subsubsection{Primary Textbook}
\textbf{Reinforcement Learning: An Introduction} (2nd Ed) by Sutton \& Barto\\
Free online: \url{http://incompleteideas.net/book/}

Essential Chapters (330 pages):
\begin{itemize}
    \item Chapter 1: The RL Problem (pp. 1-26) \Essential
    \item Chapter 2: Multi-arm Bandits (pp. 31-52) \Essential
    \item Chapter 3: Finite MDPs (pp. 53-88) \Essential $\star$
    \item Chapter 4: Dynamic Programming (pp. 89-112) \Essential
    \item Chapter 5: Monte Carlo Methods (pp. 113-142) \Essential
    \item Chapter 6: Temporal-Difference Learning (pp. 143-166) \Essential $\star$
\end{itemize}

\subsubsection{Online Resources}
\textbf{David Silver RL Course} (UCL/DeepMind) \Essential\\
10 lectures available on YouTube

\textbf{Alternative}: Hugging Face Deep RL Course (more practical)

\subsubsection{Hands-On Project}
\textbf{Project 12: Classic RL Environments} \Essential
\begin{itemize}
    \item Implement Q-learning on GridWorld
    \item Train CartPole with DQN
    \item Use OpenAI Gym/Gymnasium
\end{itemize}

\section{Phase 6: Deep RL \& RLHF (Months 17-18)}

\subsection{Month 17-18: Deep Reinforcement Learning \Essential}

\subsubsection{Advanced RL Topics}
\textbf{Deep Reinforcement Learning Hands-On} (3rd Ed, 2024) by Maxim Lapan

Essential Chapters:
\begin{itemize}
    \item Ch 6-8: DQN and Extensions \Essential
    \item Ch 9-13: Policy Gradient Methods \Essential
    \begin{itemize}
        \item PPO (Proximal Policy Optimization) \Essential $\star$
    \end{itemize}
    \item Ch 14-16: Continuous Control \Essential
    \begin{itemize}
        \item SAC (Soft Actor-Critic) \Essential $\star$
    \end{itemize}
    \item Ch 21-22: RLHF for LLMs \Essential $\star$
\end{itemize}

\subsubsection{Key Papers \Essential}
\begin{enumerate}
    \item \textbf{DQN} - "Playing Atari with Deep RL" (Mnih et al., 2013)
    \item \textbf{PPO} - "Proximal Policy Optimization" (Schulman et al., 2017) $\star$
    \item \textbf{SAC} - "Soft Actor-Critic" (Haarnoja et al., 2018) $\star$
    \item \textbf{InstructGPT} - RLHF methodology (Ouyang et al., 2022) $\star$
\end{enumerate}

\subsubsection{Projects}
\textbf{Project 13: Deep RL Algorithms} \Essential
\begin{itemize}
    \item Train DQN on Atari
    \item Train PPO on continuous control
    \item Train SAC on robotic tasks
    \item Use Stable-Baselines3
\end{itemize}

\textbf{Project 14: RLHF Pipeline} \Essential
\begin{itemize}
    \item Fine-tune language model with human feedback
    \item Use Hugging Face TRL library
    \item Train reward model
    \item PPO fine-tuning
\end{itemize}

\section{Phase 7: Production ML \& MLOps (Months 19-21)}

\subsection{Month 19-20: MLOps Foundations \Essential}

\subsubsection{Primary Textbook}
\textbf{Designing Machine Learning Systems} by Chip Huyen\\
\textit{ESSENTIAL for enterprise roles}

Critical Chapters (350 pages):
\begin{itemize}
    \item Chapter 3: Data Engineering Fundamentals (pp. 59-94) \Essential
    \item Chapter 5: Feature Engineering (pp. 129-162) \Essential
    \item Chapter 6: Model Development (pp. 163-208) \Essential
    \item \textbf{Chapter 7: Model Deployment \& Prediction Service} (pp. 209-248) \Essential $\star$
    \begin{itemize}
        \item Model compression (quantization, pruning, distillation)
        \item Cloud vs edge deployment
    \end{itemize}
    \item \textbf{Chapter 8: Data Distribution Shifts \& Monitoring} (pp. 249-286) \Essential $\star$
    \item Chapter 9: Continual Learning (pp. 287-324) \Essential
    \item Chapter 10: Infrastructure \& Tooling (pp. 325-362) \Essential
\end{itemize}

\subsubsection{Coursera Course}
\textbf{Machine Learning Engineering for Production (MLOps) Specialization}\\
DeepLearning.AI - Andrew Ng \Essential $\star$

4 courses covering:
\begin{itemize}
    \item Introduction to ML in Production
    \item ML Data Lifecycle in Production
    \item ML Modeling Pipelines in Production
    \item Deploying ML Models in Production
\end{itemize}

\begin{tcolorbox}[colback=green!10!white,colframe=green!50!black,title=Production Project]
\textbf{Project 15: End-to-End MLOps Pipeline} \Essential\\
Build production ML system with:
\begin{itemize}
    \item MLflow, DVC, Docker, Kubernetes
    \item Data versioning with DVC
    \item Experiment tracking with MLflow or W\&B
    \item Model serving with Triton or TorchServe
    \item Monitoring with Prometheus + Grafana
    \item CI/CD with GitHub Actions
    \item Deploy to AWS SageMaker or GCP Vertex AI
    \item A/B testing implementation
\end{itemize}
\end{tcolorbox}

\subsection{Month 21: Distributed Training \& Model Optimization \Essential}

\subsubsection{Model Optimization Techniques}
\textbf{Quantization} \Essential
\begin{itemize}
    \item FP32 → FP16 → INT8
    \item Post-training quantization (PTQ)
    \item Quantization-aware training (QAT)
    \item Tools: PyTorch Quantization, TensorRT, ONNX Runtime
\end{itemize}

\textbf{Pruning} \Essential
\begin{itemize}
    \item Structured vs unstructured
    \item 30-50\% size reduction typical
\end{itemize}

\textbf{Knowledge Distillation} \Essential
\begin{itemize}
    \item Teacher → Student models
    \item BERT → DistilBERT example
\end{itemize}

\subsubsection{Distributed Training}
\textbf{DeepSpeed} (Microsoft) \Essential $\star$
\begin{itemize}
    \item ZeRO optimizer for large models
    \item Essential for LLM training
\end{itemize}

\textbf{Horovod} (Uber) \Essential
\begin{itemize}
    \item Multi-GPU/multi-node training
    \item Ring-AllReduce algorithm
\end{itemize}

\textbf{PyTorch DDP} (Distributed Data Parallel) \Essential

\subsubsection{Hands-On Projects}
\textbf{Project 16: Model Optimization Challenge} \Essential
\begin{itemize}
    \item Baseline: Large transformer model
    \item Apply quantization (FP32 → INT8)
    \item Apply pruning (30\% sparsity)
    \item Apply distillation (train smaller student)
    \item Benchmark: latency, throughput, accuracy
    \item Deploy optimized model
\end{itemize}

\textbf{Project 17: Distributed Training} \Essential
\begin{itemize}
    \item Train large model across multiple GPUs
    \item Use DeepSpeed or Horovod
    \item Multi-node setup (cloud GPUs)
    \item Monitor with Weights \& Biases
\end{itemize}

\section{Phase 8: Specialization \& Applied Research (Months 22-24)}

\subsection{Month 22-23: Advanced Specialization}
Choose 2 focus areas from the following options:

\subsubsection{Option A: 3D Vision \& Neural Rendering \Desirable}
\textbf{Key Papers:}
\begin{itemize}
    \item NeRF - Neural Radiance Fields (ECCV 2020)
    \item 3D Gaussian Splatting (SIGGRAPH 2023) $\star$
\end{itemize}

\textbf{Project:} Implement NeRF or Gaussian Splatting on custom dataset

\subsubsection{Option B: Diffusion Models \& Generative AI \Essential}
\textbf{Key Papers:}
\begin{itemize}
    \item Stable Diffusion (Latent Diffusion Models)
    \item DiffiT (ECCV 2024) - SOTA diffusion with ViT
    \item ControlNet for controlled generation
\end{itemize}

\textbf{Project:} Train diffusion model, implement text-to-image or image editing

\subsubsection{Option C: Advanced NLP - LLM Agents \& RAG \Essential}
\textbf{Topics:}
\begin{itemize}
    \item Agentic RAG - Autonomous information retrieval
    \item LLM tool use and function calling
    \item Multi-agent systems
    \item Long-context models (100K+ tokens)
\end{itemize}

\textbf{Project:} Build production-grade RAG system with agents

\subsubsection{Option D: Robotics \& RL Applications \Desirable}
\textbf{Resources:}
\begin{itemize}
    \item PyBullet, MuJoCo environments
    \item Learning Dexterous In-Hand Manipulation (OpenAI)
\end{itemize}

\textbf{Project:} Train robot manipulation task with PPO/SAC

\subsection{Month 24: Portfolio Completion \& Job Preparation}

\subsubsection{Final Portfolio Projects}
\textbf{Project 18: Research Paper Implementation} \Essential
\begin{itemize}
    \item Choose recent CVPR/ICCV/NeurIPS 2024/2025 paper
    \item Implement from scratch
    \item Reproduce results
    \item Write technical blog post
    \item Open-source on GitHub
\end{itemize}

\textbf{Project 19: End-to-End Production System} \Essential\\
Build showcase project demonstrating full stack:
\begin{itemize}
    \item Research component (SOTA model)
    \item Production deployment (Docker, Kubernetes, cloud)
    \item Monitoring and continual learning
    \item Web interface (Gradio, Streamlit, or custom)
    \item Documentation and tests
\end{itemize}

Example projects:
\begin{itemize}
    \item Multi-modal search engine (CLIP + vector DB)
    \item LLM-powered code assistant with RAG
    \item Real-time video analysis system (SAM 2 + YOLO)
    \item Personalized recommendation system with RL
\end{itemize}

\subsubsection{Job Application Preparation}
\textbf{Technical Preparation:}
\begin{itemize}
    \item[$\square$] LeetCode Medium problems (2-3 per week)
    \item[$\square$] System design for ML systems
    \item[$\square$] Practice explaining papers to non-experts
    \item[$\square$] Mock technical interviews
\end{itemize}

\textbf{Portfolio \& Resume:}
\begin{itemize}
    \item[$\square$] GitHub with 5+ substantial projects
    \item[$\square$] Technical blog with deep-dive posts
    \item[$\square$] Resume highlighting implementations from scratch
    \item[$\square$] LinkedIn profile optimized for AI roles
\end{itemize}

\chapter{Complete Resource Index}

\section{Essential Textbooks (Priority Order)}

\subsection{Tier 1 - Absolutely Essential}
\begin{enumerate}
    \item \textbf{Deep Learning} by Goodfellow, Bengio, Courville [FREE] $\star$\\
    Chapters 5-10 (pp. 100-425)\\
    \url{https://www.deeplearningbook.org/}
    
    \item \textbf{Speech and Language Processing} by Jurafsky \& Martin (3rd Ed, 2025) [FREE] $\star$\\
    Chapters 9, 10, 11, 12\\
    \url{https://web.stanford.edu/~jurafsky/slp3/}
    
    \item \textbf{Designing Machine Learning Systems} by Chip Huyen [\$50] $\star$\\
    Chapters 3, 5-10\\
    Essential for production roles
    
    \item \textbf{Reinforcement Learning: An Introduction} by Sutton \& Barto [FREE] $\star$\\
    Chapters 1-6, 9, 11\\
    \url{http://incompleteideas.net/book/}
\end{enumerate}

\subsection{Tier 2 - Highly Recommended}
\begin{enumerate}[start=5]
    \item \textbf{Mathematics for Machine Learning} by Deisenroth et al. [FREE]\\
    Chapters 2-7\\
    \url{https://mml-book.github.io/}
    
    \item \textbf{Computer Vision: Algorithms and Applications} by Szeliski (2nd Ed) [FREE]\\
    Chapter 5 (Deep Learning)\\
    \url{https://szeliski.org/Book/}
    
    \item \textbf{Hands-On Machine Learning} by Géron (3rd Ed, 2024) [\$60]\\
    Chapters 1-4, 10-11, 14-16
    
    \item \textbf{Natural Language Processing with Transformers} by Tunstall et al. [\$60]\\
    Chapters 1-3, 5, 8
    
    \item \textbf{Deep RL Hands-On} by Lapan (3rd Ed, 2024) [\$50]\\
    Chapters 6-16, 21-22
\end{enumerate}

\textbf{Total Essential Textbook Cost:} \$210 (many are free)

\section{Coursera Courses}

\subsection{Year 1 Courses}
\begin{table}[h!]
\centering
\begin{tabularx}{\textwidth}{|X|c|c|}
\hline
\textbf{Course} & \textbf{Duration} & \textbf{Priority} \\
\hline
Mathematics for Machine Learning (Imperial) & 8 weeks & \Essential \\
Machine Learning Specialization (Stanford/DeepLearning.AI) & 3 months & \Essential $\star$ \\
Deep Learning Specialization (DeepLearning.AI) & 5 months & \Essential $\star$ \\
Computer Vision Specialization (CU Boulder, 2025) & 4 months & \Essential \\
NLP Specialization (DeepLearning.AI) & 4 months & \Desirable \\
\hline
\end{tabularx}
\end{table}

\subsection{Year 2 Courses}
\begin{table}[h!]
\centering
\begin{tabularx}{\textwidth}{|X|c|c|}
\hline
\textbf{Course} & \textbf{Duration} & \textbf{Priority} \\
\hline
MLOps Specialization (DeepLearning.AI - Andrew Ng) & 4 months & \Essential $\star$ \\
MLOps Specialization (Duke) & 3 months & \Essential \\
RLHF Course (DeepLearning.AI) & Short course & \Essential \\
\hline
\end{tabularx}
\end{table}

\textbf{Total Coursera Investment:} \$500-700 over 2 years

\section{Essential Papers (Must Read)}

\subsection{Transformers \& Attention}
\begin{enumerate}
    \item \textbf{Attention Is All You Need} (Vaswani et al., 2017) \Essential $\star\star\star$
    \item \textbf{BERT} (Devlin et al., 2018) \Essential
    \item \textbf{GPT-3} (Brown et al., 2020) \Essential
    \item \textbf{InstructGPT} (Ouyang et al., 2022) \Essential $\star\star$
\end{enumerate}

\subsection{Vision}
\begin{enumerate}[start=5]
    \item \textbf{Vision Transformer (ViT)} (Dosovitskiy et al., 2021) \Essential
    \item \textbf{CLIP} (Radford et al., 2021) \Essential $\star$
    \item \textbf{Segment Anything (SAM)} (Kirillov et al., 2023) \Essential
    \item \textbf{DINOv2} (Oquab et al., 2023) \Essential
\end{enumerate}

\subsection{Reinforcement Learning}
\begin{enumerate}[start=9]
    \item \textbf{DQN} (Mnih et al., 2013) \Essential
    \item \textbf{PPO} (Schulman et al., 2017) \Essential $\star$
    \item \textbf{SAC} (Haarnoja et al., 2018) \Essential
\end{enumerate}

\section{Essential Tools \& Libraries}

\subsection{Deep Learning Frameworks}
\begin{itemize}
    \item \textbf{PyTorch} (primary) \Essential $\star$
    \item TensorFlow (secondary) \Essential
    \item JAX \Desirable
\end{itemize}

\subsection{NLP Libraries}
\begin{itemize}
    \item Hugging Face Transformers \Essential $\star$
    \item Hugging Face Datasets \Essential
    \item Hugging Face PEFT (LoRA) \Essential
    \item LangChain, LlamaIndex \Essential
\end{itemize}

\subsection{MLOps Tools}
\begin{itemize}
    \item MLflow \Essential $\star$
    \item Weights \& Biases \Essential
    \item DVC \Essential
    \item Docker, Kubernetes \Essential
    \item TensorBoard \Essential
\end{itemize}

\subsection{Model Serving}
\begin{itemize}
    \item NVIDIA Triton Inference Server \Essential $\star$
    \item TorchServe \Essential
    \item TensorFlow Serving \Essential
    \item FastAPI (API development) \Essential
\end{itemize}

\subsection{Cloud Platforms}
\begin{itemize}
    \item AWS (especially SageMaker) \Essential $\star$
    \item Google Cloud (Vertex AI) \Essential
    \item Azure ML \Desirable
\end{itemize}

\chapter{Study Schedule \& Time Management}

\section{Weekly Schedule Template}

\begin{tcolorbox}[colback=blue!5!white,colframe=darkblue,title=Weekly Time Commitment]
\textbf{Total: 25-30 hours/week}

\textbf{Weekdays (Mon-Fri): 3-4 hours/day}
\begin{itemize}
    \item Morning (1 hour): Coursera lectures
    \item Evening (2-3 hours): Textbook reading + exercises OR implementation
\end{itemize}

\textbf{Weekends: 10-15 hours total}
\begin{itemize}
    \item Saturday: 6-8 hours (deep implementation work)
    \item Sunday: 4-7 hours (projects + review)
\end{itemize}
\end{tcolorbox}

\section{Monthly Time Allocation}
\begin{itemize}
    \item 40\% Implementation (coding projects, algorithms from scratch)
    \item 30\% Theory (textbooks, papers)
    \item 20\% Coursera courses
    \item 10\% Portfolio work (documentation, blog posts)
\end{itemize}

\section{Success Milestones}

\subsection{Year 1 Quarterly Milestones}

\textbf{Q1 (Months 1-3):}
\begin{itemize}
    \item[$\square$] Completed Mathematics for ML
    \item[$\square$] Completed ML Specialization (Andrew Ng)
    \item[$\square$] Implemented linear/logistic regression from scratch
    \item[$\square$] Kaggle competition completed
\end{itemize}

\textbf{Q2 (Months 4-6):}
\begin{itemize}
    \item[$\square$] Completed Deep Learning Specialization (Courses 1-2)
    \item[$\square$] Implemented neural network from scratch (NumPy)
    \item[$\square$] Read Deep Learning (Goodfellow) Chapters 5-8
    \item[$\square$] MNIST >95\% accuracy with custom implementation
\end{itemize}

\textbf{Q3 (Months 7-9):}
\begin{itemize}
    \item[$\square$] Completed DL Specialization (Course 4)
    \item[$\square$] Implemented ResNet or ViT from scratch
    \item[$\square$] Read and understood Attention Is All You Need
    \item[$\square$] Fine-tuned vision model on custom dataset
\end{itemize}

\textbf{Q4 (Months 10-12):}
\begin{itemize}
    \item[$\square$] Completed DL Specialization (Course 5)
    \item[$\square$] Implemented Transformer from scratch
    \item[$\square$] Fine-tuned BERT and GPT models
    \item[$\square$] Built and deployed RAG system
    \item[$\square$] Portfolio website live with 5+ projects
\end{itemize}

\subsection{Year 2 Quarterly Milestones}

\textbf{Q1 (Months 13-15):}
\begin{itemize}
    \item[$\square$] Implemented CLIP-based multi-modal application
    \item[$\square$] Completed RL Fundamentals (Sutton Ch 1-6)
    \item[$\square$] Trained DQN on Atari games
    \item[$\square$] Read 8+ landmark papers
\end{itemize}

\textbf{Q2 (Months 16-18):}
\begin{itemize}
    \item[$\square$] Completed Deep RL algorithms (PPO, SAC)
    \item[$\square$] Implemented RLHF pipeline
    \item[$\square$] Advanced RL projects deployed
\end{itemize}

\textbf{Q3 (Months 19-21):}
\begin{itemize}
    \item[$\square$] Completed MLOps Specialization
    \item[$\square$] Built end-to-end MLOps pipeline
    \item[$\square$] Model optimization project completed
    \item[$\square$] Distributed training experience
\end{itemize}

\textbf{Q4 (Months 22-24):}
\begin{itemize}
    \item[$\square$] Completed specialization focus areas (2 of 4)
    \item[$\square$] Reproduced recent SOTA paper
    \item[$\square$] Final portfolio project completed
    \item[$\square$] Ready for Applied Research Engineer interviews
\end{itemize}

\chapter{Critical Success Factors}

\section{Essential vs Desirable Knowledge}

\subsection{Essential Knowledge \Essential}
\textbf{Foundations:}
\begin{itemize}
    \item Mathematics (linear algebra, calculus, probability, optimization)
    \item ML fundamentals (supervised/unsupervised learning, evaluation)
    \item Deep learning theory (backpropagation, optimization, regularization)
\end{itemize}

\textbf{Core ML:}
\begin{itemize}
    \item Neural networks from scratch
    \item CNNs and modern vision architectures (ResNet, ViT)
    \item Transformers architecture deeply
    \item Fine-tuning pre-trained models
\end{itemize}

\textbf{Domains:}
\begin{itemize}
    \item Computer Vision (CNNs, ViT, object detection, segmentation)
    \item NLP (Transformers, BERT, GPT, fine-tuning, RAG)
    \item Reinforcement Learning (DQN, PPO, SAC, RLHF)
\end{itemize}

\textbf{Production:}
\begin{itemize}
    \item MLOps (MLflow, DVC, Docker, Kubernetes)
    \item Model optimization (quantization, pruning, distillation)
    \item Model serving (Triton, TorchServe)
    \item Distributed training (DeepSpeed or Horovod)
    \item Cloud platforms (AWS SageMaker)
    \item Monitoring and CI/CD for ML
\end{itemize}

\subsection{Desirable Knowledge \Desirable}
\textbf{Advanced Topics:}
\begin{itemize}
    \item 3D vision (NeRF, Gaussian Splatting, multi-view geometry)
    \item Advanced generative models (diffusion models beyond basics)
    \item Robotics applications
    \item Video understanding
    \item Meta-learning, few-shot learning
    \item Multi-agent RL
\end{itemize}

\textbf{Tools:}
\begin{itemize}
    \item JAX framework
    \item Ray for distributed computing
    \item Advanced MLOps tools (Metaflow, Prefect)
    \item Multiple cloud platforms
    \item Edge deployment optimization
\end{itemize}

\section{What Makes This Plan Work}

\begin{enumerate}
    \item \textbf{Progressive Complexity}: Start with foundations, build to advanced topics
    \item \textbf{Theory + Practice Balance}: Every topic includes both reading and implementation
    \item \textbf{Implement from Scratch}: Builds deep understanding before using libraries
    \item \textbf{Production Focus}: Not just research, but deployment and scale
    \item \textbf{Paper Reading}: Learn to read and implement SOTA research
    \item \textbf{Portfolio Building}: Continuous documentation and project showcase
    \item \textbf{Multi-Domain Coverage}: CV, NLP, RL all covered substantively
    \item \textbf{Applied at Work}: Skills are immediately useful in current role
\end{enumerate}

\section{Common Pitfalls to Avoid}

\begin{itemize}
    \item[$\times$] Skipping fundamentals (math, backprop, optimization)
    \item[$\times$] Only using pre-trained models without understanding
    \item[$\times$] Not reading papers (only tutorials)
    \item[$\times$] Ignoring production/deployment skills
    \item[$\times$] Not implementing from scratch at least once per architecture
    \item[$\times$] Rushing through without deep understanding
    \item[$\times$] Not building portfolio projects
\end{itemize}

\chapter{Career Trajectory \& ROI}

\section{Timeline Flexibility}

\begin{table}[h!]
\centering
\begin{tabularx}{\textwidth}{|l|X|c|}
\hline
\textbf{Track} & \textbf{Description} & \textbf{Duration} \\
\hline
Intensive & 35-40 hours/week commitment & 18-20 months \\
Standard & 25-30 hours/week (as outlined) & 24 months \\
Extended & 20 hours/week if work is demanding & 30 months \\
\hline
\end{tabularx}
\end{table}

\section{Budget Summary}

\begin{table}[h!]
\centering
\begin{tabularx}{\textwidth}{|X|r|}
\hline
\textbf{Category} & \textbf{Cost} \\
\hline
Textbooks & \$210 \\
Coursera Subscription & \$500-700 \\
Cloud Computing (projects) & \$200-500 \\
\textbf{Total Investment} & \textbf{\$1,000-1,500} \\
\hline
\end{tabularx}
\end{table}

\section{Return on Investment}

\begin{table}[h!]
\centering
\begin{tabularx}{\textwidth}{|X|c|}
\hline
\textbf{Position Level} & \textbf{Salary Range} \\
\hline
Entry Applied Research Engineer & \$150K-\$180K \\
Mid-level & \$180K-\$220K \\
Senior & \$220K+ (with equity often 1.5-2x base) \\
\hline
\multicolumn{2}{|c|}{\textbf{Career Investment Return: 10-20x over career}} \\
\hline
\end{tabularx}
\end{table}

\section{When to Start Applying}

\begin{itemize}
    \item \textbf{After Month 18}: For junior/mid-level Applied Research roles
    \item \textbf{After Month 24}: For competitive senior roles at top companies
    \item \textbf{Portfolio is Key}: 5+ substantial projects more important than timeline
\end{itemize}

\chapter{Community Resources \& Continuous Learning}

\section{Stay Current}

\subsection{Essential Websites}
\begin{itemize}
    \item \textbf{arXiv.org}: Daily paper releases
    \item \textbf{Papers With Code}: \url{https://paperswithcode.com/}
    \item \textbf{Hugging Face}: \url{https://huggingface.co/}
\end{itemize}

\subsection{Key People to Follow}
Twitter/X: @karpathy, @jeremyphoward, @AK\_ML, @chipro, @ylecun

\section{Communities}

\begin{itemize}
    \item \textbf{r/MachineLearning}: Reddit community
    \item \textbf{r/learnmachinelearning}: Beginner-friendly
    \item \textbf{MLOps Community}: \url{https://mlops.community/}
    \item \textbf{Hugging Face Discord}: Active community
    \item \textbf{Fast.ai Forums}: \url{https://forums.fast.ai/}
\end{itemize}

\section{Blogs to Follow}

\begin{itemize}
    \item Lilian Weng (OpenAI): \url{https://lilianweng.github.io/}
    \item Distill.pub: \url{https://distill.pub/}
    \item Jay Alammar: \url{https://jalammar.github.io/}
    \item Chip Huyen: \url{https://huyenchip.com/}
    \item Sebastian Raschka: \url{https://sebastianraschka.com/}
\end{itemize}

\section{Continuous Learning Beyond 2 Years}

\begin{itemize}
    \item Read 2-3 papers per week from arXiv
    \item Implement SOTA models within 3 months of paper release
    \item Contribute to open-source ML libraries
    \item Write technical blog posts
    \item Attend conferences (NeurIPS, CVPR, ICML - virtual options)
    \item Mentor others in the community
\end{itemize}

\vspace{2cm}

\begin{tcolorbox}[colback=yellow!10!white,colframe=orange!75!black,title=Final Note]
\textbf{This plan represents approximately 1,200-1,500 hours of focused study over 24 months.}

Success requires discipline, consistency, and genuine passion for the field. Your engineering background and 5 years of CV experience provide a strong foundation—this plan will transform you into a competitive candidate for Applied AI/ML Research Engineer roles at top enterprise companies.

\textbf{Remember}: The goal is not just to complete the plan, but to deeply understand each concept and build a portfolio that demonstrates your capabilities. Quality over speed.

\textbf{Good luck on your journey!} 🚀
\end{tcolorbox}

\end{document}