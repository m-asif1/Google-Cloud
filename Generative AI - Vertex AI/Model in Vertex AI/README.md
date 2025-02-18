## **Gemini 1.5 Pro Model in Vertex AI**

### **Overview**
[Gemini 1.5 Pro](https://deepmind.google/technologies/gemini/pro/) is a new language model from the Gemini family. This model introduces a breakthrough long context window of up to 1 million tokens that can help seamlessly analyze large amounts of information and long-context understanding. It can process text, images, audio, video and code all together for deeper insights. In this lab, you will learn how to use the Gemini API in Vertex AI to work with the Gemini 1.5 Pro model.

#### Prerequisites

Before starting, you should be familiar with:
- Basic Python programming.
- General API concepts.
- Running Python code in a Jupyter notebook on [Vertex AI Workbench](https://cloud.google.com/vertex-ai/docs/workbench/introduction).

How to use Gemini 1.5 Pro to:
- Analyze audio for insights.
- Understand videos (including their audio components).
- Extract information from PDF documents.
- Process images, video, audio and text simultaneously.

### How to start Google Cloud console
- **Open Google Cloud console** use your Google Cloud account credentials
- Google Cloud console opens in this tab
- To access Google Cloud products and services, click the **Navigation menu** or type the service or product name in the **Search field**.
![alt text](images/image.png)

### **Open the notebook in Vertex AI Workbench**

1. In the Google Cloud console, on the **Navigation menu**, click **Vertex AI > Workbench**.
2. Find the `Workbench instance name` instance and click on the **Open JupyterLab** button.
3. The JupyterLab interface for your Workbench instance opens in a new browser tab.


### **Set up the notebook**
1. Open the `notebook name` file.
4. In the **Select Kernel** dialog, choose **Python 3** from the list of available kernels.
3. Run through the **Getting Started** and the **Import libraries** sections of the notebook.

### **Experiment with Audio understanding**
Gemini 1.5 Pro can directly process audio for long-context understanding.
- Run through the **Audio understanding** of the notebook.

**Experiment with Video with audio understanding**
Gemini 1.5 Pro's native multimodal and long context capabilities on video interleaving with audio inputs.
1. Run through the **Video with audio understanding** of the notebook.

### **Experiment with PDF document analysis**
Gemini 1.5 Pro to process PDF documents, and analyze content, retain information, and provide answers to queries regarding the documents.

1. Run through the **PDF document analysis** of the notebook.

### **Experiment with All modalities (images, video, audio, text) at once**

Gemini 1.5 Pro is natively multimodal and supports interleaving of data from different modalities. So, in this section, try out how Gemini 1.5 Pro can support a mix of audio, visual, text, and code inputs in the same input sequence.

1. Run through the **All modalities (images, video, audio, text)** of the notebook.