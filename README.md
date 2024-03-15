# B12-4: Graph Neural Networks for Enhancing Sentiment Analysis

In this study, we want to introduce a novel approach to sentiment analysis by integrating Graph Neural Networks (GNNs), specifically Graph Attention Networks (GAT), with traditional Natural Language Processing (NLP) techniques. By focusing on the challenges of interpreting long-range dependencies within text, particularly in the context of social media interactions, we propose a model that leverages the relational and textual information present
in data from college SubReddit forums before and during the COVID-19 pandemic (Yan and Liu 2021). Our methodology employs RoBERTa for text embedding, followed by a GAT to incorporate the structural relationships between messages, enhancing the sentiment analysis capability beyond the limitations of conventional models. The results demonstrate a statistically significant improvement in identifying and relating sentiments across distant text
parts, underscoring the potential of GNNs in capturing complex interactions
within text data. This research contributes to the evolving field of sentiment
analysis by showcasing the effectiveness of combining GNNs with existing
NLP frameworks, offering insights into the nuanced emotional landscape of
digital communications during a global crisis.

## Environment Setup

Ensure you have Python 3.6.8 and tensorflow-gpu 1.15 installed on your system. This project is tested on Python 3.6.8 and tensorflow-gpu 1.15.


### Virtual Environment (Recommended)

It's recommended to use a virtual environment to manage dependencies and avoid conflicts with other projects.

- **Creating a virtual environment:**
  ```bash
  python -m venv venv
  ```

- **Activating the virtual environment:**
  - On Windows:
    ```bash
    .\venv\Scripts\activate
    ```
  - On macOS and Linux:
    ```bash
    source venv/bin/activate
    ```

### Installing Dependencies

Install all required dependencies by running:

```bash
pip install -r requirements.txt
```

## Running the Project

0. **Download Data:**
   - [Go to Additional Dataset section](#additional-dataset) to download the datasets and put them into the `path\\to\\directory\\data` folder on Windows, or `path/to/directory/data` folder if you are on Linux/MacOS.
   - If you are using Linux/MacOS instead of windows, you might want to refector the path in the project, for example, replace every occurence of `\\` with `/`, an example would be replacing `C:\\Users\\yunfa\\dsc180b\\` with `C:/Users/yunfa/dsc180b/`.
   - For every occurence of `C:\\Users\\yunfa\\dsc180b\\`, use `Ctrl` + `F` to find and replace them with the directory where you cloned this project. For example, say Trevor's operating system can't find the specified path: `path_preprocessed="C:\\Users\\yunfa\\dsc180b\\data"`, he can replace every occurence of  `C:\\Users\\yunfa\\dsc180b\\` with the `path\\to\\directory` where he cloned this project, say `C:\\Users\\trevor\\dsc180b\\`. The new path_processed would be thus defined `path_preprocessed="C:\\Users\\trevor\\dsc180b\\data"`. Again, on Linux/MacOS this example paths would be `C:/Users/trevor/dsc180b/data` instead.

2. **Preprocessing Steps:**
   - Run the preprocessing notebooks `0-Preprocessing1.ipynb` and `1-Preprocessing2.ipynb` in order. These notebooks prepare your data for training.

3. **Model Training:**
   - Execute `2-GAT_CrossValidation.ipynb` for model training and validation.
  
4. **Model Predicting:**
   - Execute `3-GatPrediction.ipynb` for model training and prediction.

5. **Ensemble Model Predicting:**
   - Execute `4-EnsemblePrediction.ipynb` for final ensemble model training and prediction.

6. **Additional Scripts:**
   - `base_gattn.py`, `gat.py`, `jhyexp.py`, `layers.py`, `process.py`, and `process_ppi.py` are modules used within the notebooks. Ensure they are in the same directory as the notebooks or appropriately referenced.

## Additional Notes

- Make sure to adjust paths within the scripts and notebooks according to your directory structure.
- For any issues related to TensorFlow versions or compatibility, refer to the official TensorFlow documentation.

## Contributors

Yuxin Guo, Yujia Wang, Yunfan Long

## Reference

### Code reference and baseline template

+ [Sentiment-Analysis-Post-COVID19](https://github.com/AlvaYan/postCOVIDSentiAnalysis)

+ [Sentiment-Analysis-GNN-During-COVID19](https://github.com/AlvaYan/Sentiment-Analysis-GNN-During-COVID19)

### Paper reference in implementation

+ [COVID-19 sentiment analysis using college subreddit data](https://arxiv.org/abs/2112.04351)

## Additional Dataset

You can downloaded the unprocessed anonymized data [here](https://drive.google.com/file/d/13PzwBAjyI4VYpCEVye6fU3gGsDvdnrBY/view?usp=sharing)

You can download the RoBERTa processed data and score [here](https://drive.google.com/file/d/1RRi5o1JCWeuS-dfhNOuxsk7JxJXKBOuL/view?usp=sharing)

