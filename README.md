# DSC180B-B12: GraphATTEncode

In this study, we want to introduce a novel approach to sentiment analysis by integrating Graph Neural Networks (GNNs), specifically Graph Attention Networks (GAT), with traditional Natural Language Processing (NLP) techniques. By focusing on the challenges of interpreting long-range dependencies within text, particularly in the context of social media interactions, we propose a model that leverages the relational and textual information present
in data from college SubReddit forums before and during the COVID-19 pandemic (Yan and Liu 2021). Our methodology employs RoBERTa for text embedding, followed by a GAT to incorporate the structural relationships between messages, enhancing the sentiment analysis capability beyond the limitations of conventional models. The results demonstrate a statistically significant improvement in identifying and relating sentiments across distant text
parts, underscoring the potential of GNNs in capturing complex interactions
within text data. This research contributes to the evolving field of sentiment
analysis by showcasing the effectiveness of combining GNNs with existing
NLP frameworks, offering insights into the nuanced emotional landscape of
digital communications during a global crisis.

## Environment Setup

Ensure you have Python 3.7 or newer installed on your system. This project is tested on Python 3.7, 3.8, and 3.9.

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

1. **Preprocessing Steps:**
   - Run the preprocessing notebooks `0-Preprocessing1.ipynb` and `1-Preprocessing2.ipynb` in order. These notebooks prepare your data for training.

2. **Model Training:**
   - Execute `2-GAT_CrossValidation.ipynb` for model training and validation.

3. **Additional Scripts:**
   - `base_gattn.py`, `gat.py`, `jhyexp.py`, `layers.py`, `process.py`, and `process_ppi.py` are modules used within the notebooks. Ensure they are in the same directory as the notebooks or appropriately referenced.

4. **Running Custom Scripts:**
   - For running Python scripts (e.g., `gat.py`), use:
     ```bash
     python gat.py
     ```

## Additional Notes

- Make sure to adjust paths within the scripts and notebooks according to your directory structure.
- For any issues related to TensorFlow versions or compatibility, refer to the official TensorFlow documentation.

## Contributors

Yuxin Guo, Yujia Wang, Yunfan Long
