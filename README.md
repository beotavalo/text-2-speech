# Text to Speech Deployment with BentoML

This repository provides a framework for deploying a **Text-to-Speech** application using [BentoML cloud](https://www.bentoml.com/), a powerful platform for serving AI models and applications. 

## Getting Started

### Cloning the Repository

To replicate this project, you need to clone the repository to your local machine. Use the following command in your terminal:

```bash
git clone https://github.com/beotavalo/text-2-speech.git
```

Once cloned, navigate into the project directory:

```bash
cd text-2-speech
```
## Package Management and Virtual Environment with UV


### Deploying the TTS Service

#### Step 1: Install BentoML library

Make sure you have Python≥3.8, install bentoml package locally with:


```bash
pip install -U bentoml
```

For more details on BentoML, visit their [Documentation](https://docs.bentoml.com/en/latest/?_gl=1*kwqrh4*_gcl_au*MzMxMDczNzA3LjE3NDU4MDA3NTY) page.

#### Step 2: Login to BentoCloud

To deploy the application in the cloud, you need to log in to BentoCloud. BentoCloud is a fully-managed platform for running AI applications.

Run the following command and create an API token following the instructions:

```bash
bentoml cloud login
```

This command will redirect you to create an account on BentoCloud and generate an API key. Follow the instructions to complete the login process.

#### Step 3: Deploy the Application

Once logged in, deploy your Text-to-Speech application using the following command:

```bash
bentoml deploy .
```

This command will:

1. Push the necessary images to BentoCloud.
2. Build the environment using the images.
3. Download the TTS model.
4. Initialize the server to serve the application.

#### Step 4: Access Your Deployed Service

After deployment, BentoCloud will provide you with an endpoint URL to access your TTS service. You can use this endpoint to send text input and receive audio output.

## Contributing

Feel free to contribute to this repository by submitting issues or pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## References:
- [Cloud deployment](https://docs.bentoml.com/en/latest/get-started/cloud-deployment.html)
- [BentoML: MLOps for Beginners](https://www.kdnuggets.com/bentoml-mlops-for-beginners)
- [BentoML Hello world Example](https://docs.bentoml.com/en/latest/get-started/hello-world.html)
