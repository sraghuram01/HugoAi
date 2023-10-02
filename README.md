# HugoAi

<p align="center">
  <img width="863" alt="Screenshot 2023-06-18 at 19 43 24" src="https://github.com/Hteam121/HugoAi/assets/85576231/88412901-9244-43a8-9cf9-581b19425fb8">
</p>

## Resources Used

Throughout this project, we utilized numerous resources for our AI models, server hosting, development environment, and others:

1. Python 3.8.10: The Python version used for our AI models.
2. [Flask](https://flask.palletsprojects.com/en/2.0.x/): A micro web framework written in Python. It's our choice for the backend.
3. [fastai](https://docs.fast.ai/): A deep learning library which provides high-level components that can quickly and easily provide state-of-the-art results in standard deep learning domains.
4. [Digital Ocean](https://www.digitalocean.com/): A cloud infrastructure provider, used for server hosting.
5. [Google Colab](https://colab.research.google.com/): A Python development environment that runs in the browser using Google Cloud.
6. [Kaggle](https://www.kaggle.com/datasets/nih-chest-xrays/data): The source of our dataset.
7. [pyenv](https://github.com/pyenv/pyenv): A Python version management tool.
8. [Nginx](https://nginx.org/en/): An HTTP and reverse proxy server.
9. [HTML/CSS/JavaScript](https://developer.mozilla.org/en-US/docs/Learn): The frontend technologies used to design the web application.


## Description
This project was executed under the Artificial Intelligence Mentorship Program at the University of Texas at Dallas. Our team of seven members, comprising Shaik Hatim, Faris Shaik, Sanya Oak, Varun Raghuram, and Arrio Gonsalves, along with our mentors Anusha Saha and Poorna Bharanikumar, created four simple chest X-ray models. These models can detect pathological conditions, age, gender, and viewing positions. The project spanned over a six-week program where we delved into AI and Machine Learning.

The models were initially designed to detect pathological conditions. However, with some tweaking, they can easily be extended to cover the other three areas. 

The models were implemented as a web application using HTML, CSS, and JavaScript. Google Colab was used as the development environment.

The project is hosted on Digital Ocean, which provided us with valuable learning experiences about cloud server management, security, and deployments. Our journey with Python version management was particularly insightful. Given that our models were Python version-specific, we needed to ensure the correct version of Python (3.8.10) was installed and available. We encountered challenges initially but overcame them by setting up a virtual environment (venv) using pyenv. This isolated environment allowed us to work with the required Python version without conflicts.

We used the Flask framework to develop the backend of our application. Flask's simplicity and flexibility allowed us to set up a web-based API that managed the execution environment for our models. In our Flask application, we defined routes for image upload and implemented methods to serve model predictions. We also ensured secure handling of image files. The predictions were generated using multiple models (pathological condition, gender, age, and viewing position classifiers) from the fastai library, which were loaded into the application at startup. These predictions were then returned to the client as a JSON response.

An additional major challenge was handling the extensive dataset sourced from Kaggle. We initially attempted to use S3 for this purpose but were unsuccessful due to the time and processing requirements. Consequently, we condensed the dataset into a 30k image sample set, which accurately represents the original data.

From configuring Python environments to managing firewall settings and understanding the essentials of web servers with Nginx, the application's deployment gave us real-world insights into server administration. We also worked with SSL certificates and domain mapping, redirecting the IP address to our chosen domain.

Digital Ocean's robust and easy-to-use platform made it feasible to handle a high-traffic web application powered by AI models. Unfortunately, we had to terminate the live site as it used up our resources. However, feel free to browse through our demo [here](https://github.com/Hteam121/HugoAi/tree/master/demo).

## Resources
1. [National Institutes of Health Chest X-Ray Dataset](https://www.kaggle.com/datasets/nih-chest-xrays/data)
2. [Multi-category Classification of Various Chest Conditions from Chest X-Rays](https://towardsdatascience.com/multi-category-classification-of-various-chest-conditions-from-chest-x-rays-1d6428522997)

## Dataset
The project uses the National Institutes of Health Chest X-Ray Dataset, consisting of 112,120 X-ray images with disease labels from 30,805 unique patients. 

### Data limitations:
1. The image labels are NLP extracted, so there could be some erroneous labels, but the NLP labeling accuracy is estimated to be >90%.
2. There are very limited numbers of disease region bounding boxes (See BBox_list_2017.csv).
3. Chest x-ray radiology reports are not anticipated to be publicly shared. 

### File contents
Please refer to the [Kaggle dataset](https://www.kaggle.com/datasets/nih-chest-xrays/data) for detailed file contents.

### Class descriptions
The dataset features 15 classes: 14 diseases and one for "No findings". Images can be classified as "No findings" or one or more disease classes. 

## Set Up and Installation
1. Clone this GitHub repository
2. Install the necessary dependencies listed in the `requirements.txt` file
3. To interact with the server, use the following command:
    ```
    ssh root@192.168.0.1
    ```
4. You can find additional server management commands in the [Server Commands](#server-commands) section.

## Server Commands
Here are some useful terminal commands for managing the server:
- SSH into the server: `ssh root@<IP Address>`
- Activating the virtual environment: `source bin/activate`
- Installing dependencies: `pip3.8 install -r requirements.txt`
- Activating the Python version for the project: `pyenv activate venv_3.8.10`

## Acknowledgments
- [Shaik Hatim](https://www.linkedin.com/in/shaik-hatim/)
- [Faris Shaik](https://www.linkedin.com/in/farisshaik/)
- [Varun Raghuram](https://www.linkedin.com/in/varun-raghuram-2a7822201/)
- [Arrio Gonsalves](https://www.linkedin.com/in/adgarrio/)
- [Sanya Oak](https://www.linkedin.com/in/sanyaoak/)
- [Anusha Saha](https://www.linkedin.com/in/anushasaha/)
- [Poorna Bharanikumar](https://www.linkedin.com/in/poorna-bharanikumar/)
- And the rest of the AI Mentorship Program team at the University of Texas at Dallas.

