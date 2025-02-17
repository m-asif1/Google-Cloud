[test](https://cdn.qwiklabs.com/zjN7W3mhXjZNtCFZb4Y1PAfOK%2FadVx5lXhKNC7vLYcg%3D)

7. On the top right of the Prompt section, click Insert media > Upload. Upload the timetable image you downloaded. The media can be in the form of an image, video, text, or audio file.

8. Here is a detailed description of the image:
9. Describe the image. Replace the previous prompt with the following and click the **Submit** button.


   > Describe the image in detail.
  

The image shows a departure board, likely at an airport or train station. It displays the scheduled departure times and destinations for various flights or trains. The board appears to be digital, with illuminated orange text on a dark background.

Here's a breakdown of the visible details:

*   **Time and Destination**: Each line shows a scheduled departure time followed by the destination city.
*   **Destinations**: The destinations listed include Moscow (SVO), Edinburgh, London (LHR and LGW), Bucharest (OTP), Kiev (Borispol), Dublin, East Midlands, Sofia, Newcastle, St. Petersburg, and Manchester.
*   **Time**: The departure times range from 10:50 to 12:45.
*   **Color**: The text is illuminated in orange.
*   **Background**: The background is dark.
*   **Setting**: The image hints at an airport or train station setting.

In the background, there is a structural framework, possibly the ceiling of the building. It's made of steel with a blue-gray hue.

10. Tune the parameter. In the Configuration section, adjust the temperature by scrolling from left (0) to right (2). Resubmit the prompt to observe any changes in the outcome compared to the previous result.

**Note:** Temperature controls the degree of randomness in token selection. Lower temperatures are good for prompts that expect a true or correct response, while higher temperatures can lead to more diverse, unexpected, or potentially biased results. With a temperature of 0 the highest probability token is always selected.

11. Extract the text from the image. Replace the previous prompt with the following:
> Read the text in the image.

Here are the bounding box detections:
```json
[
  {"box_2d": [16, 360, 57, 458], "label": "10:50"},
  {"box_2d": [59, 360, 105, 460], "label": "11:05"},
  {"box_2d": [106, 363, 155, 463], "label": "11:05"},
  {"box_2d": [159, 363, 210, 463], "label": "11:10"},
  {"box_2d": [447, 317, 505, 456], "label": "12:30"},
  {"box_2d": [581, 313, 628, 413], "label": "12:40"},
  {"box_2d": [643, 311, 697, 415], "label": "12:40"},
  {"box_2d": [712, 273, 772, 418], "label": "12:45"},
  {"box_2d": [10, 485, 65, 661], "label": "MOSCOW"},
  {"box_2d": [49, 486, 109, 655], "label": "EDINBURGH"},
  {"box_2d": [99, 488, 160, 609], "label": "LONDON"},
  {"box_2d": [147, 491, 216, 650], "label": "BUCHAREST"},
  {"box_2d": [319, 491, 377, 619], "label": "KIEU"},
  {"box_2d": [440, 498, 503, 619], "label": "LONDON"},
  {"box_2d": [509, 495, 569, 605], "label": "NEWCASTLE"},
  {"box_2d": [577, 502, 633, 678], "label": "ST PETERSBURG"},
  {"box_2d": [638, 500, 701, 623], "label": "LONDON"},
  {"box_2d": [710, 471, 776, 637], "label": "MANCHESTER"},
  {"box_2d": [10, 660, 55, 734], "label": "SUO"},
  {"box_2d": [99, 611, 152, 722], "label": "LHR"},
  {"box_2d": [147, 648, 208, 780], "label": "OTP"},
  {"box_2d": [317, 622, 371, 873], "label": "BORISPOL"},
  {"box_2d": [438, 622, 498, 687], "label": "LGW"},
  {"box_2d": [638, 621, 696, 684], "label": "LGW"}
]
```
Further on, if you want to format the output to a list, replace the previous prompt with the following:
> Parse the time and city in this image into a list with two columns: time and city.

Here's the list of times and cities from the image:

| Time  | City              |
|-------|--------------------|
| 10:50 | MOSCOW/SVO       |
| 11:05 | EDINBURGH          |
| 11:05 | LONDON/LHR         |
| 11:10 | BUCHAREST/OTP      |
| 11:30 | KIEV/BORISPOL      |
| 11:35 | DUBLIN             |
| 11:45 | EAST MIDLANDS      |
| 12:15 | SOFIA              |
| 12:30 | LONDON/LGW         |
| 12:30 | NEWCASTLE          |
| 12:40 | ST PETERSBURG     |
| 12:40 | LONDON/LGW         |
| 12:45 | MANCHESTER         |

Your turn - try out some different prompts! How do these results differ from before?

  12. Analyze the information on the image. Replace the previous prompt with the following:
      >  Calculate the percentage of the flights to different continents.
      
Here's a breakdown of the flight destinations by continent and the percentage of flights to each:

**Flights Listed:**

*   Moscow/SVO (Russia): Europe/Asia (Russia is transcontinental)
*   Edinburgh (UK): Europe
*   London/LHR (UK): Europe
*   Bucharest/OTP (Romania): Europe
*   Kiev/Borispol (Ukraine): Europe
*   Dublin (Ireland): Europe
*   East Midlands (UK): Europe
*   Sofia (Bulgaria): Europe
*   London/LGW (UK): Europe
*   Newcastle (UK): Europe
*   St Petersburg (Russia): Europe
*   London/LGW (UK): Europe
*   Manchester (UK): Europe

**Continent Count:**

*   Europe: 13
*   Asia: 1 (Russia)

**Percentage Calculation:**

*   Total Flights: 14
*   Europe: (13 / 14) * 100% = 92.86%
*   Asia: (1 / 14) * 100% = 7.14%
*   Europe/Asia (Russia): (1 / 14) * 100% = 7.14%

**Summary:**

*   **Europe: Approximately 92.86%**
*   **Asia: Approximately 7.14%**

Does the result meet your expectations? You are highly encouraged to try different prompts for various tasks. You are also encouraged to experiment with different temperature settings to observe the changes in the result.

13. Once you finish the prompt design, **save** the prompt by clicking Save on the top right of the Configuration section. For the region, select `**us-east4**` from the dropdown and then confirm by clicking **Save**.

14. To find your saved prompts, on the left-hand navigation menu, navigate to **Prompt Management**.
```
**Note**: After selecting **Save**, give the prompts a few seconds to properly save and then proceed further with the lab. Click "Try again" if prompted "failed to update history."
```
