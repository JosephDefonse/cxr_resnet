<div id="top"></div>
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h1 align="center">Chest X-ray Disease Classification Using ResNet</h1>
  <p align="center">
    A deep learning approach for classifying 14 thoracic diseases using Chest X-ray images, leveraging the ResNet architecture for feature extraction and classification.
    <br /> <br/>
    <b>The academic research paper we are referencing is below:</b>
    <br>
    <a href="https://arxiv.org/abs/1705.02315">View Paper</a>
</div>

---

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#key-features">Key Features</a></li>
        <li><a href="#technologies">Technologies & Methodologies</a></li>
      </ul>
    </li>
    <li>
      <a href="#repository-contents">Repository Contents</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li>
      <a href="#results">Results</a>
    </li>
    <li>
      <a href="#roadmap">Roadmap</a>
    </li>
    <li>
      <a href="#contact">Contact</a>
    </li>
    <li>
      <a href="#references">References</a>
    </li>
  </ol>
</details>

---

<!-- ABOUT THE PROJECT -->
<h2 id="about-the-project"> About The Project </h2>

This project focuses on the classification of **14 thoracic diseases** from **Chest X-ray (CXR) images** using a **deep learning-based approach**. We leverage the **ResNet** architecture for classification and introduce several enhancements to improve performance, interpretability, and analysis beyond existing research.

### Key Achievements:
- **Outperformed the Official Paper**: Achieved **higher AUC scores** in most disease categories.
- **Mathematical Analysis of ResNet**: Detailed **forward propagation and backpropagation derivations**, including their relationship to the **vanishing gradient problem**.
- **Comprehensive Exploratory Data Analysis (EDA)**:
  - Identified anomalies such as **unrealistic Patient Age and Follow-Up values**.
  - Provided **detailed explanations** for all dataset graphs to demonstrate a strong understanding of data distribution and biases.
- **Custom Implementation of ResNet-18 from Scratch**:
  - Built a **fully custom ResNet-18 model** to showcase theoretical understanding, rather than using pre-built PyTorch models.
  - Highlighted **key differences** in implementation from standard ResNet-18.
- **Detailed Breakdown of Code and Model Components**:
  - **Dataset Preparation & Processing**:
    - Loading and cleaning the dataset.
    - Extracting unique labels and computing **positive weights** for **Weighted BCE Loss**.
    - Implementing **train-validation-test split** to prevent data leakage.
    - Applying **data transformations and augmentations**.
    - Creating **data loaders** for training and testing.
  - **ResNet Model Implementation**:
    - **Images as Tensor Representation**
    - **Convolution Layer Operations**
    - **Pooling Strategies**
    - **Covariate Shift & Internal Covariate Shift Analysis**
    - **Batch Normalization Theory**
    - **Linear Layer and Fully Connected Network**
    - **Activation Function (ReLU) Breakdown**
  - **Mathematical Derivations**:
    - **Weighted Binary Cross-Entropy (BCE) Loss Function** derivation and importance.
    - **Adam Optimizer** formula breakdown and impact on gradient updates.
- **Advanced Model Evaluation & Interpretability Enhancements**:
  - **AUC-ROC Curve for Each Disease Class**: Direct comparison with the **original academic paper**.
  - **Bounding Box Algorithm Using Feature Maps**:
    - Extracted **heatmaps** from the **final feature layer** of ResNet.
    - Generated bounding boxes for **disease localization**.
    - Compared results against the **actual bounding box annotations**, showing strong alignment despite minor deviations.

<p align="right">(<a href="#top">back to top</a>)</p>

---

<h2 id="technologies"> Technologies & Methodologies </h2>

This project integrates state-of-the-art deep learning techniques with rigorous theoretical analysis.

- **Technologies**:
  - Python
  - **PyTorch** (ResNet model implementation)
  - **NumPy & Pandas** (data handling)
  - **OpenCV** (bounding box detection & visualization)
  - **Matplotlib & Seaborn** (visualization)
  - **SciPy & Scikit-learn** (evaluation metrics)

- **Methodologies**:
  - **Custom-built ResNet-18** implementation for transparency and theoretical clarity.
  - **Multi-label classification** using **Weighted Binary Cross-Entropy Loss**.
  - **Gradient-based feature map extraction** for interpretability.
  - **Addressed dataset imbalance** using class-based weight adjustments.
  - **Benchmarking against the ChestX-ray8 dataset**, ensuring fair performance comparisons.

<p align="right">(<a href="#top">back to top</a>)</p>

---

<h2 id="repository-contents"> Repository Contents </h2>

- **`main.ipynb`**: The code training, testing and evaluating the model.
- **`Deep Learning Based Medical Image Classification.pdf`**: The report on this project.
- **`my_resnet_model.pth`**: The pre-trained model saved.

<p align="right">(<a href="#top">back to top</a>)</p>

---

<!-- GETTING STARTED -->
<h2 id="getting-started"> Getting Started </h2>

To replicate or extend this project locally, follow these steps:

<h3 id="installation"> Installation </h3>

#### Step 1: Use Kaggle Code Notebook
- Sign up for an account at [Kaggle](https://www.kaggle.com/) if you haven't already.
- Go to **Settings** and confirm your phone number to enable GPU access.
- Kaggle currently provides **30 hours of free GPU usage per week** (as of writing this).

#### Step 2: Upload the Jupyter Notebook
- Download `main.ipynb` from this repository.
- Upload it to your Kaggle **Code** environment.

#### Step 3: Enable GPU
- Open **Kaggle Code** and start a new notebook.
- In the **Settings** panel, select **GPU (T4 x2)** as the accelerator.

#### Step 4: Run the Notebook
- Execute the cells in `main.ipynb` to preprocess the dataset, train the model, and evaluate the results.

<h2 id="results"> Results </h2>

The model was evaluated using the **AUC-ROC metric** and compared against published benchmarks. The results demonstrate **improved classification accuracy** in multiple thoracic disease categories. Full results and visualizations can be found in the **`Deep Learning Based Medical Image Classification.pdf`** document under Section 7: 'Results & Evaluation'.

<h2 id="roadmap"> Roadmap </h2>

* Improve model interpretability with additional explainable AI techniques.
* Improve model accuracy to reach models such as from <a href="https://www.researchgate.net/publication/370591019_Multi-Level_Residual_Feature_Fusion_Network_for_Thoracic_Disease_Classification_in_Chest_X-Ray_Images"> Li Qiang </a> in his paper and <a href="https://github.com/paloukari/NIH-Chest-X-rays-Classification"> Spyros Garyfallos </a> in his writeup.
<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->
<h2 id="contact"> Contact </h2>
Email: shean.defonjo@gmail.com

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- REFERENCES -->
<h2 id="references"> References </h2>

Wang, X., Peng, Y., Lu, L., Lu, Z., Bagheri, M., & Summers, R. M. (2017). **ChestX-ray8: Hospital-scale chest X-ray database and benchmarks on weakly-supervised classification and localization of common thorax diseases.** [arXiv:1705.02315](https://arxiv.org/abs/1705.02315).

All additional references can be found in the report.

<p align="right">(<a href="#top">back to top</a>)</p>
