# 📘 Module 03 – Deep Learning & Neural Networks

---

## 1️⃣ Trainer’s Lesson Notes

**Definition:**  
Deep Learning is a subset of Machine Learning that uses **Artificial Neural Networks (ANNs)** to automatically extract complex patterns from raw data (e.g., pixels of an image).  

**Key points:**
- Unlike ML, deep learning does not require manual feature engineering → the network learns its own internal representations.  
- Handles **large datasets** efficiently with parallel processing (mini-batches, GPUs).  
- Enables scalability and high performance for complex tasks.  

**Artificial Neural Networks (ANNs):**
- **Layers:** Input, hidden, output.  
- **Neurons:** Basic computational units.  
- **Weights:** Define strength of connections.  
- **Activation Functions:** Introduce non-linearity (ReLU, Sigmoid, etc.).  
- **Bias:** Adds flexibility to neuron outputs.  
- **Training:** Forward pass → prediction → error → backpropagation → weight update.  

**History:**  
- 1950s: Perceptrons, artificial neurons.  
- 1980s: Backpropagation.  
- 1990s: Convolutional Neural Networks (CNNs).  
- 2000s: Rise of GPUs → large-scale training.  
- 2012: AlexNet breakthrough, Deep-Q-Network.  
- 2016+: Generative AI, Transformers, LLMs.  

**Key Architectures:**
- Feedforward Neural Networks (MLP).  
- CNN → image/video analysis.  
- RNN → sequential/time-series data.  
- LSTM → long-term dependencies.  
- Autoencoders → feature extraction, anomaly detection.  
- GANs → generative models (images, audio, text).  
- Transformers → state-of-the-art NLP (translation, LLMs).  

**Applications:**
- **Images:** Object detection, medical imaging, self-driving cars.  
- **Text:** Translation, summarization, sentiment detection.  
- **Audio:** Music generation, speech recognition.  
- **Generative:** Text-to-image, synthetic data.  

**Deep Dive into CNNs:**
- Designed for grid-like data (images).  
- **Layers:**  
  - Convolutional (feature detector)  
  - Activation (pattern highlighter, e.g., ReLU)  
  - Pooling (dimension reducer)  
  - Fully connected → classification  
  - Softmax → probabilities  
  - Dropout → prevent overfitting  
- **Limitations:** Expensive, black-box, overfitting risk, sensitive to input noise.  

**Practical Demo:**  
- Dataset → `make_circles` (two concentric circles).  
- MLPClassifier (scikit-learn).  
- Low neurons → poor classification.  
- More neurons → complex decision boundary, better accuracy.  
- Backpropagation adjusts weights iteratively.  

---

## 2️⃣ Extra Clarity (Simple Analogies)

- **ANN:** Like a factory assembly line – each layer extracts a piece of the product (features).  
- **Neuron:** A worker checking inputs and deciding whether to pass forward.  
- **CNN:** Like a house inspector – zooms into rooms, checks walls, then summarizes findings.  
- **Overfitting:** Memorizing past exam answers but failing new questions.  
- **Backpropagation:** Teacher correcting homework → adjusts weights like giving feedback.  
- **ReLU:** Switch – only passes useful signals forward.  

---

## 3️⃣ DevOps Angle (AIOps)

- **CNNs:** Detect anomalies in monitoring dashboards (spikes, visual anomalies).  
- **RNNs/LSTMs:** Predict future server load from time-series metrics.  
- **Autoencoders:** Detect unusual patterns in logs → anomaly detection.  
- **GANs:** Generate synthetic logs/test data for simulations.  
- **Transformers:** Summarize incident reports, auto-generate runbooks.  

OCI Tie-in:
- OCI **Data Science Service** → train custom ANN models.  
- OCI **Vision Service** → CNNs for OCR/object detection.  
- OCI **Language Service** → transformers for NLP.  

---

## 4️⃣ Exam Focus

- **DL vs ML:** DL = automatic feature extraction, ML = manual feature engineering.  
- **Key Architectures:** CNN (images), RNN/LSTM (sequences), Transformer (NLP).  
- **Training:** Backpropagation adjusts weights.  
- **Overfitting:** Complex model memorizes training data.  
- **CNN Components:** Convolution → ReLU → Pooling → Fully Connected → Softmax.  
- **Applications:** Image classification, sentiment analysis, speech recognition.  

---

## 5️⃣ Beyond Certification

- **AWS equivalents:** Rekognition, Polly, Translate, SageMaker.  
- **GCP equivalents:** Vision API, Vertex AI, Speech-to-Text.  
- **OSS equivalents:** TensorFlow, PyTorch, HuggingFace Transformers.  
- **Industry adoption:**  
  - Tesla → self-driving (CNNs).  
  - Netflix → recommendations (RNN/Transformers).  
  - OpenAI → LLMs (Transformers).  

---

## 6️⃣ Resume Booster

**Resume Bullet Example:**  
> “Implemented a deep learning classifier (MLP/CNN) using Python and Scikit-learn to separate complex datasets, visualizing decision boundaries. Compared model accuracy with traditional ML approaches and explored OCI Vision AI service integration.”  

**Mini-project idea:**  
- Build an MLP to classify concentric circle dataset (`make_circles`).  
- Train with different hidden layer sizes → visualize boundaries.  
- Optional: Upload simple CNN demo (MNIST digit classification).  

---

## 7️⃣ Fast-Track Notes

- DL = subset of ML using neural nets.  
- ANN = layers, neurons, weights, activation, bias.  
- Training = forward pass + backpropagation.  
- CNN = vision, RNN = sequence, Transformer = NLP.  
- Overfitting vs Underfitting.  
- Applications: images, text, audio, generative AI.  

---

## 📸 Screenshots (Mini-Tests & Practice)

| Test        | Screenshot    | Notes                                      |
|-------------|---------------|--------------------------------------------|
| Quiz 1      | mini-test-03  | History & evolution of deep learning       |
| Results     | questions     | ✅ Passed with 100%                        |

---
