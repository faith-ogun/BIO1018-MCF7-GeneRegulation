# BIO1018: Using Neural Networks to Understand Gene Regulation in the MCF7 Breast Cancer Cell Line

## Project Description
This project aims to predict gene expression from chromatin accessibility data using neural networks in the MCF7 breast cancer cell line. The project involves preprocessing ATAC-seq and RNA-seq data, building machine learning models, and evaluating their performance.

This project contains part of the work completed for my 8-week final disseration project.

It leverages the GET model from Xi "Alexander" Fu's paper in Nature and contains the implementation of the model described in our paper: https://www.nature.com/articles/s41586-024-08391-z.

## Motivation and Background
The motivation for this project stems from the growing need for computational methods to understand gene regulation in cancer biology. Transcriptional regulation plays a pivotal role in cancer development and progression, making it crucial to explore gene expression mechanisms in well-established cancer models like the MCF-7 breast cancer cell line.

The **MCF7 cell line** is a widely used model in breast cancer research due to its luminal-like characteristics and responsiveness to estrogen. By combining chromatin accessibility (ATAC-seq) and RNA-seq data, we can uncover novel regulatory elements and improve gene expression prediction using neural networks.

This project aligns with my broader research interests in **machine learning and cancer biology**, with the ultimate goal of pursuing a **PhD in machine learning for cancer research**. My passion lies in integrating computational models with biological data to uncover new therapeutic targets and improve precision oncology.

---

## Project Workflow
The project is divided into the following stages:
1. **Data Preprocessing**: Cleaning and preparing ATAC-seq and RNA-seq data for analysis.
2. **Model Training**: Training neural networks to predict gene expression.
3. **Evaluation**: Assessing model performance using metrics such as Pearson correlation, R², and Spearman correlation with WandB.
4. **Interpretation**: Analyzing important features and regulatory elements contributing to gene expression.

---

## Directory Structure
- `dataset/`: Raw and unprocessed data files.
- `notebooks/`: Jupyter notebooks for data exploration.

Please view notebooks to see my process and completed pipeline.

## How to Run the Project
a. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/BIO1018-MCF7-GeneRegulation.git
   ```

b. Set up the environment using the Singularity container:
  ```bash
  singularity exec get_complete_latest.sif python scripts/preprocess.py
  ```

c. Pull from Docker and run Jupyter Notebook:
  ```bash
  docker pull faithogun/get_complete:latest

  docker run --entrypoint /bin/bash -it -v $(pwd):$(pwd) get_complete

  docker run -it -p 8888:8888 -v $(pwd):/workspace  get_complete  jupyter notebook --allow-root --ip 0.0.0.0 --no-    browser --NotebookApp.token='' --NotebookApp.password='' --notebook-dir=$(pwd)
```

## Key Findings

## Future Work
The next phase of this project will focus on expanding the neural network’s predictive capabilities and integrating additional data modalities. The overall goal is to build a model that predicts chromatin accessibility and gene expression in the MCF7 cell line using both ATAC-seq and RNA-seq data.

### Phase Two Objectives:
1. **Build a Neural Network for Chromatin Accessibility Prediction**  
   - Develop a binary classification model to distinguish open vs. closed chromatin regions using ATAC-seq data.
   - Optimize and evaluate the model’s performance using metrics such as accuracy, precision, recall, and F1-score.

2. **Integrate RNA-seq Data for Gene Expression Prediction**  
   - Combine ATAC-seq and RNA-seq data to enhance prediction accuracy.  
   - Modify the neural network architecture to accept multi-modal inputs and predict continuous gene expression levels.  
   - Explore feature importance to identify key chromatin regions and RNA-seq signals driving predictions.

3. **Model Optimization and Validation**  
   - Fine-tune the combined model, focusing on robustness and generalizability.  
   - Perform k-fold cross-validation and test the model on external datasets for reliability.  
   - Utilize feature attribution methods (e.g., SHAP values) to interpret model predictions.

4. **Final Documentation and Presentation**  
   - Document the model architecture, preprocessing pipeline, and training process in a comprehensive Jupyter notebook.  
   - Prepare plots, visual summaries, and presentation materials for the dissertation submission.

---

### Key Milestones for Future Work:
- **Week 1:** Build and train a neural network for chromatin accessibility prediction.  
- **Week 2:** Integrate RNA-seq data and expand the neural network for joint modeling.  
- **Week 3:** Optimize, validate, and prepare final documentation for reproducibility and presentation.

---

### Best Practices for Phase Two:
- **Version Control:** Use Git to track code changes and experiments.  
- **Data Management:** Keep data organized and backed up in multiple locations.  
- **Daily Check-ins:** Review progress daily to stay on track and adjust the plan as needed.

You can find Phase Two here:

## Link to Final Dissertation Paper:
- add once complete

## Citation
A foundation model of transcription across human cell types. Nature (2024). https://doi.org/10.1038/s41586-024-08391-z

## Acknowledgments
Special thanks to my research mentors and colleagues in the Furney Group at RCSI, for their invaluable support and guidance throughout this project.

## Contact
For questions, please contact, faith.ogundimu2@mail.dcu.ie or faithogundimu@rcsi.com.
To discuss offering an internship opportunity, please email, faithogun12@gmail.com.

