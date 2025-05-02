Multi-Industry Resume Classification Using LDA
This project explores topic modeling for resumes across multiple industries using Latent Dirichlet Allocation (LDA). The goal is to extract meaningful themes while refining stopword filtering to improve coherence scores.
 Dataset
* Source: Kaggle (search for �resume dataset�)
* Type: Resumes from various industries
* Preprocessing: Tokenization, stopword removal, lemmatization

 Project Workflow
1  Data Preprocessing
* Removed standard and resume-specific stopwords (e.g., "summary," "skills," "position")
* Applied lemmatization & tokenization
* Structured document-term matrix for LDA modeling
2  Topic Modeling Using LDA
* Optimized num_topics, passes, and iterations
* Evaluated topic coherence scores dynamically
* Visualized topics using PyLDAVis
3  Results & Insights
* Improved coherence scores by fine-tuning stopword selection
* Achieved better topic separation across industries
* Next steps: Exploring BERTopic for more adaptive classification

Installation & Usage
Install dependencies
pip install -r requirements.txt
Run the LDA model
I installed Miniconda3 from which I worked on Jupyter Lab. 

LDA_single_par_set.ipynb
		runs a preset directory of resumes through the LDA model with single set of values of parameters: number of top frequent words, number of topics, number of passes.  Plots visualization of derived topics with pyLDAvis. Calculates coherence score.

LDA_multiple_par_set.ipynb
		runs a preset directory of resumes through the LDA model looping over multiple sets of values of parameters: number of top frequent words, number of topics, number of passes. Calculates coherence scores for each set and determines the best set of parameters (with maximal coherence score).

Visualize Topics
		only with LDA_single_par_set.ipynb

Results & Next Steps
Refined stopword filtering improved coherence scores
Effective topic separation for resume classification: coherence score on some profession datasets barely tips coherence score of .50, however on most sets it is below par.
Future improvements: Experimenting with BERTopic, refining preprocessing further

Contributing
Feel free to fork the repo, suggest improvements, or collaborate! ??
Contact me on LinkedIn for discussions on NLP optimizations.

