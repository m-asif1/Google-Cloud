## **Vertex AI Studio**

### **Overview**
**Vertex AI** is a comprehensive machine learning development platform that provides both **predictive** and **generative AI** capabilities. It allows you to train, evaluate, and deploy predictive machine learning models for forecasting purposes. Additionally, you can utilize the platform to discover, tune, and serve generative AI models to produce content.

[Vertex AI](https://cloud.google.com/generative-ai-studio) Studio lets you quickly test and customize **generative AI** models so you can leverage their capabilities in your applications. It provides a variety of tools and resources including both UI (user interface) and coding examples that make it easy to start with generative AI, even if you don't have a background in machine learning.

This lab guides you through Vertex AI Studio, where you'll unlock the potential of cutting-edge generative AI models. You'll explore Gemini and use it to analyze images, design prompts, and generate conversations directly on the Google Cloud console. No need for API or Python SDKs - it's all accessible through the intuitive user interface.

How to:
- Analyze images with Gemini
- Explore Vertex AI Studio Freeform mode
- Design text prompts for zero-shot, one-shot, and few-shot prompting
- Generate conversations with chat prompts

#### **How to start Google Cloud console**
- **Open Google Cloud console** use your Google Cloud account credentials
- Google Cloud console opens in this tab
- To access Google Cloud products and services, click the **Navigation menu** or type the service or product name in the **Search** field.
![alt text](images\image.png)

### **Analyze images with Gemini in Freeform mode**
use Gemini to analyze an image and extract information from it. In Freeform mode, you can design prompts for various tasks such as classification, extraction, and generation. There is no conversation history in Freeform mode, so every prompt is a brand-new request to the model.

#### Enable the Vertex AI API
1. In the Google Cloud console, enter **Vertex AI API** in the top search bar.
2. Click on the result for **Vertex AI API** under Marketplace & APIs.
3. Click **Enable**.

![alt text](images\image-1.png)

#### Analyze images with Gemini
1. In the Google Cloud console, from the **Navigation menu**, select **Vertex AI > Vertex AI Studio > Overview**.
![alt text](images\image-2.png)

2. Under **Generate with Gemini**, click **Open Freeform**.

The UI contains three main sections:

- **Prompt** (located in the center): Here, you can create a prompt that utilizes multimodal capabilities.
- **Configuration** (located on the right): This section allows you to select models, configure parameters, and obtain the corresponding code.
- **Response** (located at the bottom): This section displays the results of your prompt.

![alt text](images\image-3.png)

3. On the top left, click **Untitled Prompt** and rename your prompt as `Image Analysis`.
4. In the **Configuration** section on the top right, click on the **Model** dropdown then select the `model name` model.
5. For **Region**, select `Region`.
6. Timetable image save it to your desktop.

![alt text](images\image-4.png)

7. On the top right of the **Prompt** section, click **Insert media > Upload**. Upload the timetable image you downloaded. The media can be in the form of an image, video, text, or audio file.

![alt text](images\image-5.png)

8. The image will be displayed inside of the **Prompt** section. Copy the following text and paste it under the image and click on the **Submit** button on the bottom right of the Prompt section.
```
Title the image.
```
**Response**
> Airport departure board.


Or be more specific:
```
Title the image in 3 words.
```
**Response**
> Airport Departure Board

Does the title meet your expectations? Try to modify the prompt to see if you get different results.

9. Describe the image. Replace the previous prompt with the following and click the **Submit** button.
```
Describe the image in detail.
```

**Response**
```
Here is a detailed description of the image:

The image shows a close-up of an electronic departure board, likely at an airport or train station. The board displays departure times and destinations in an orange, dot-matrix style font. The background of the board is black.

On the board, the following information is visible, from top to bottom:

10:50 - MOSCOW/SVO
11:05 - EDINBURGH
11:05 - LONDON/LHR
11:10 - BUCHAREST/OTP
11:30 - KIEV/BORISPOL
11:35 - DUBLIN
11:45 - EAST MIDLANDS
12:15 - SOFIA
12:30 - LONDON/LGW
12:30 - NEWCASTLE
12:40 - ST PETERSBURG
12:40 - LONDON/LGW
12:45 - MANCHESTER
In the background, out of focus, there's a glimpse of the architectural structure, possibly the ceiling of the building. It appears to be made of metal beams, suggesting a modern or industrial-style building. The colors are predominantly blue and gray.
```


10. Tune the parameter. In the Configuration section, adjust the temperature by scrolling from left (0) to right (2). Resubmit the prompt to observe any changes in the outcome compared to the previous result.

```
Note: Temperature controls the degree of randomness in token selection. Lower temperatures are good for prompts that expect a true or correct response, while higher temperatures can lead to more diverse, unexpected, or potentially biased results. With a temperature of 0 the highest probability token is always selected.
```
11. Extract the text from the image. Replace the previous prompt with the following:

```
Read the text in the image.
```
**Response**

Here are the bounding box detections:

```json
[
  {"box_2d": [156, 529, 210, 860], "label": "BUCHAREST/OTP"},
  {"box_2d": [324, 510, 373, 873], "label": "EAST MIDLANDS"},
  {"box_2d": [449, 317, 502, 453], "label": "12:30"},
  {"box_2d": [646, 291, 698, 425], "label": "12:40"},
  {"box_2d": [578, 501, 630, 880], "label": "ST PETERSBURG"},
  {"box_2d": [387, 508, 437, 620], "label": "SOFIA"},
  {"box_2d": [0, 377, 54, 472], "label": "10:50"},
  {"box_2d": [268, 341, 321, 470], "label": "11:10"},
  {"box_2d": [63, 543, 102, 700], "label": "EDINBURGH"},
  {"box_2d": [207, 527, 262, 793], "label": "KIEU BORISPOL"},
  {"box_2d": [446, 510, 497, 679], "label": "LONDON"},
  {"box_2d": [646, 493, 696, 791], "label": "LONDON/LGW"},
  {"box_2d": [262, 525, 317, 654], "label": "KIEU"},
  {"box_2d": [387, 333, 439, 451], "label": "12:15"},
  {"box_2d": [712, 477, 770, 793], "label": "MANCHESTER"},
  {"box_2d": [578, 295, 626, 423], "label": "12:40"},
  {"box_2d": [66, 364, 107, 464], "label": "11:05"},
  {"box_2d": [514, 505, 566, 775], "label": "NEWCASTLE"},
  {"box_2d": [63, 364, 105, 410], "label": "11"},
  {"box_2d": [107, 547, 156, 718], "label": "LONDON"},
  {"box_2d": [712, 279, 766, 412], "label": "12:45"},
  {"box_2d": [507, 310, 561, 435], "label": "12:30"},
  {"box_2d": [5, 533, 58, 708], "label": "MOSCOW/SUO"}
]
```


Further on, if you want to format the output to a list, replace the previous prompt with the following:

```
Parse the time and city in this image into a list with two columns: time and city.
```
**Response**

Here's a list of the time and city information from the image:
---
| Time  | City           |
|-------|-----------------|
| 10:50 | MOSCOW/SUO     |
| 11:05 | EDINBURGH      |
| 11:05 | LONDON/LHR     |
| 11:10 | BUCHAREST/OTP  |
| 11:30 | KIEU BORISPOL  |
| 11:35 | NITANI       |
| 11:45 | EAST MIDLANDS |
| 12:15 | SOFIA          |
| 12:30 | NEWCASTLE      |
| 12:40 | ST PETERSBURG  |
| 12:40 | LONDON/LGW     |
| 12:45 | MANCHESTER     |
---
Your turn - try out some different prompts! How do these results differ from before?

12. Analyze the information on the image. Replace the previous prompt with the following:

```
Calculate the percentage of the flights to different continents.
```
**Response**
---
Here's the breakdown and calculation:

**1. Identify Destinations:**

*   **Europe:** Edinburgh, London, Bucharest, Kiev, Dublin, East Midlands, Sofia, Newcastle, St. Petersburg, Manchester, Moscow

**2. Continent Count:**

*   **Flights to Europe:** 11

**3. Calculate the Percentage:**

*   Total number of flights: 12
*   Percentage of flights to Europe = (11/12)*100 = 91.6%

**Answer:** 91.6% of flights are to the continent of Europe.
---

Does the result meet your expectations? You are highly encouraged to try different prompts for various tasks. You are also encouraged to experiment with different temperature settings to observe the changes in the result.

13. Once you finish the prompt design, save the prompt by clicking **Save** on the top right of the Configuration section. For the **region**, select Region from the dropdown and then confirm by clicking **Save**.

14. To find your saved prompts, on the left-hand navigation menu, navigate to **Prompt Management**.

> **Note**: After selecting **Save**, give the prompts a few seconds to properly save and then proceed further with the lab. Click "Try again" if prompted "failed to update history."

### **Explore multimodal capabilities**
In addition to **images, text**, and **audio**, Gemini is capable of accepting **videos** as inputs and generating text as an output.
1. Navigate to **Cloud Storage > Buckets** and copy the name of your Cloud Storage bucket and save it to use in the further step.
2. Click Activate **Cloud Shell Activate** at the top of the Google Cloud console.
3. In your Cloud Shell terminal, run the command below to copy the sample video `gs://spls/gsp154/video/train.mp4`( [preview](https://storage.googleapis.com/spls/gsp154/video/train.mp4) ) to your Cloud Storage bucket. Replace `<Your-Cloud-Storage-Bucket>` with the bucket name you copied earlier.
```
gcloud storage cp gs://spls/gsp154/video/train.mp4 gs://<Your-Cloud-Storage-Bucket>
```
> **Note**: Make sure to replace the <Your-Cloud-Storage-Bucket> with your bucket name.
4. From the **Navigation menu** , select **Vertex AI > Vertex AI Studio > Overview**.
5. Under **Generate with Gemini**, click **Open Freeform**.
6. In the **Configuration section** on the top right, click on the **Model** dropdown then select the `model name` model.
7. For **Region**, select `Region`.
8. Click **Insert Media > Import from Cloud Storage**.
9. Click on your bucket name and then click on the sample video i.e., `train.mp4` and click **Select**.
10. Generate information about the video by inserting the following prompt and clicking the **Submit** button.
```
Title the video.
```
**Response**
---
Here's a title for the video:

**Train Passing by in the Rain**
---
---

Freeform mode offers many capabilities such as writing stories from images, analyzing videos, and generating multimedia ads. Explore more freeform use cases by clicking **Prompt gallery8*. Check out more information about [design multimodal prompts](https://cloud.google.com/vertex-ai/docs/generative-ai/multimodal/design-multimodal-prompts).

### **Design text prompts**
Explore designing text prompts in Vertex AI Studio. You will explore zero-shot, one-shot, and few-shot prompting.

### Prompt design
You can feed your desired input text, e.g. a question, to the model. The model will then provide a response based on how you structured your prompt. The process of figuring out and designing the best input text (prompt) to get the desired response back from the model is called **Prompt Design**.

**Prompt design methods**

There are three main methods to design prompts:

- **Zero-shot prompting** - This is a method where the LLM is given only a prompt that describes the task and no additional data. For example, if you want the LLM to answer a question, you just prompt "what is prompt design?".
- **One-shot prompting** - This is a method where the LLM is given a single example of the task that it is being asked to perform. For example, if you want the LLM to write a poem, you might give it a single example poem.
- **Few-shot prompting** - This is a method where the LLM is given a small number of examples of the task that it is being asked to perform. For example, if you want the LLM to write a news article, you might give it a few news articles to read.

**Parameters**          

Temperature and Token limit are two important parameters that you can adjust to influence the model's response.

- **Temperature** controls the randomness in token selection. A lower temperature is good when you expect a true or correct response. A temperature of 0 means the highest probability token is always selected. A higher temperature can lead to diverse, unexpected, or potentially biased results. The `model name` model has a temperature range of 0 - 2 and a default of 1.
- **Output token limit** determines the maximum amount of text output from one prompt. A token is approximately four characters.

## Zero-shot prompting
Try zero-shot prompting in Free-form mode.

1. Navigate back to the **Vertex AI Studio > Overview** page and click **Open Freeform**.
2. On the top right under **Model**, select the `model name` model.
3. For **Region**, select `Region`.
4. Copy the following over to the prompt input field.
```
What is a prompt gallery?
```
5. Click on the **Submit** button.

The model will respond to a comprehensive definition of the term prompt gallery.

Here are some exploratory exercises to explore.

- Adjust the `Output Token limit` parameter to `1024` and click the **SUBMIT** button.
- Adjust the `Temperature` parameter to `0.5` and click the **SUBMIT** button.
- Adjust the `Temperature` parameter to `2.0` and click the **SUBMIT** button.

Inspect how the responses change as to change the parameters.

### One-shot prompting

You can design prompts in more organized ways. You can provide **Context** and **Examples** in their respective input fields. One-shot prompting is a method where the model is given a single example of the task that it is being asked to perform. In this section, you will ask the model to complete a sentence.

1. Start by removing any text from the **Prompt** box.
2. Inside of the **Prompt** box, click **Add examples**. This will open a new window where you can add examples for the prompt.

![alt text](images\image-6.png)

3. Add this to the **INPUT** field:
```
The color of the grass is
```
4. Add this to the **OUTPUT** field:
```
The color of the grass is green
```
5. Click on the **Add examples** button.
6. In the **Test** field, copy the following in the **Input** field.
```
The color of the sky is
```
7. Click on the **Submit** button. You should receive a response from the model similar to the following.
```
The color of the sky is blue
```
Instead of completing the sentence, the model gave a full sentence as a response since you provided an example for the model to base its output from. To change the response to simply complete the sentence, you can adjust the example provided in the **OUTPUT** field.

8. Click the **Examples** button in the **Prompt** box and change the **OUTPUT** field to:
```
Green
```
9. Click on the **Add examples** button.
10. In the **Test** field, copy the following in the **Input** field.
```
The color of the sky is
```
11. Click on the **Submit** button. You should receive a response from the model similar to the following:
```
blue
```
You can see that the model now completes the sentence based on the example you provided. You have successfully influenced the way the model produces response.

### Few-shot prompting
For the next practice, you will use the model to perform sentiment analysis on a sentence, such as determining whether a movie review is positive or negative using few-shot prompting.

1. In the **Prompt*** field, delete your examples from the previous section. To delete your examples, hover over the **Examples** and click the **X** (Remove File) button.

![alt text](images\image-7.png)

2. Click the **Add examples** button to add more examples.
3. Add the following examples:

| INPUT      | OUTPUT |
| ----------- | ----------- |
| A well-made and entertaining film      | positive |
| I fell asleep after 10 minutes         | negative |
| The movie was ok                       | neutral |

4. Once you have added the examples, click on the **Add examples** button.

![alt text](images\image-8.png)

5. In the **Test** field, copy the following in the **Input** field.
```
It was a time well spent!
```
> positive

6. Click on the **Submit** button.

![alt text](images\image-9.png)

The model now provides a sentiment for the input text. For the text It was a time well spent!, the sentiment is labeled as positive.

7. Once you finish the prompt design, name the prompt as `Sentiment Analysis`.

### **Generate conversations**
Chat mode is a conversational mode that allows you to have a freeform chat with the model. The model uses the conversation history as context for future responses. In this section, you will create a chat prompt and have a conversation with the model.

1. From the left menu, navigate to **Chat** to create a new chat prompt.
2. On the top right under **Model**, select the **model name** model.
3. For **Region**, select `Region`.

For this section, you will add context to the chat and let the model respond based on the context provided.

4. Click System instructions and add the following context:
```
Your name is Roy.
You are a support technician of an IT department.
You only respond with "Have you tried turning it off and on again?" to any queries.
```
5. Insert the following prompt:
```
My computer is so slow! What should I do?
```
6. Click the **Submit** button.

The model should respond with the following:
```
Have you tried turning it off and on again?
```
7. In **System instructions**, click **Clear value**.
8. Click **System instructions** and add the following context.
```
Your name is Roy.
You are a support technician of an IT department.
You are here to support the users with their queries.
```
9. Insert the following prompt.
```
My computer is so slow! What should I do?
```
10. Click the **Submit** button.

The model should now be more helpful in its response to the user query.

Feel free to experiment with different prompts and context to see how the model responds. You can also add more context to the chat prompt to see how the model responds based on the context provided.




