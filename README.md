<div id="top"></div>

<!-- PROJECT LOGO -->
<br />
<div align="center">

  <h3 align="center">Chatbot</h3>

  <p align="center">
    Simple Retrieval-based & Generative-based chatbot in order to make conversation. 🗣
    <br />
    <a href="https://github.com/sepehrgh98/Chatbot"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    .
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary> 
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#parts">Parts</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project

<p> <img src="https://user-images.githubusercontent.com/52400040/203013191-db480723-17f3-4812-9e0b-e4c3d75cf57a.jpg" width="600"> </p>  

 In this project, two kind of chatbot have been implemented.

 *   Retrival_based

  This chatbot uses context to answer questions. Every asking questions are answerd based on contexes from wikipedia. This chatbot is capable to recognize and answer questions with different structures and different words. 


 *   Generative_based

  This chatbot recognizes questions and ask them itself. There is a seq-to-seq structure used to extract features from questions and produce answers.

<p align="right">(<a href="#top">back to top</a>)</p>


### Built With

Major frameworks/libraries used to this project:

* [python 3.8](https://www.python.org/)
* [tensorflow , keras](https://www.tensorflow.org/)
* [gpiozero]( https://gpiozero.readthedocs.io/en/stable/)
* [numpy](https://numpy.org/)
<p align="right">(<a href="#top">back to top</a>)</p>



<!-- PARTS -->
## Parts

**Data preparation and augmentation**

*   Retrival_based

    In this project biographies of 500 well-known people in the world were used as dataset. All of this biographies was colleted from WikiPedia.


*   Generative_based

    In this project a dataset of conversations in Amazon website is used. This dataset includes about 320,000 Q&A pairs which was collected from convertions between cosumers and operators. The word representation method in this project was dictionary lookup.
     . So after creating a collection of used words and allocating index to each word, the process of learning started. This dictionary also was useful in test stage to convert indexes to words.


**Pre-processing**

*   Retrival_based

1.  All the texts were separated sentence by sentence
2.  Remove words which do not have much impact on the train process
3.  Create a dictionary from remained words (useful in both train and test stage)

*   Generative_based

1.  All the Q&A pairs were separated sentence by sentence
2.  Remove words which do not have much impact on the train process
3.  Creating a collection of used words and allocating index to each word

**Model**

RNN based sequence to sequence model. 
<p> <img src="https://user-images.githubusercontent.com/52400040/203071066-15558f0e-f0cb-4a7b-bd66-cd53203dcd96.png" width="500"> </p>


For each cell LSTM is used.

<p> <img src="https://user-images.githubusercontent.com/52400040/203071213-b0fca244-f631-49cc-8a6d-276e3c8d50f2.png" width="500"> </p>

The model is designed to support the attention model.

<p> <img src="https://user-images.githubusercontent.com/52400040/203071359-58d4c078-0807-422e-b0c5-5adb41cf6b34.jpg" width="500"> </p>




**Process**

We feed all Q&A pairs to model in rder to extract features from input. All features will be stored in a matrix named 'contex vector' which contains a summery from input by the use of attention method. Finally, the output will be created word by word by use of 'contex vector' and previous words.




<!-- CONTACT -->
## Contact

Sepehr Ghamari - [@sepehrgh98](https://github.com/sepehrgh98) - sepehrghamri@gmail.com


Project Link: [https://github.com/sepehrgh98/Speech-Recognition](https://github.com/sepehrgh98/Speech-Recognition)

<p align="right">(<a href="#top">back to top</a>)</p>


---
<div align="center">
<p>
 <img src="https://user-images.githubusercontent.com/47852354/138564509-b5dffb4e-f48b-4db5-b8a4-1385ef2b22c8.png" width="110">
 <img src="https://user-images.githubusercontent.com/47852354/138607395-e18bfc7a-204c-495a-914f-bd5cf8436ca4.jpg" width="70">
</p>
</div>

