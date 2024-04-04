<div align="center">
  <a href="https://koyeb.com">
    <img src="https://www.koyeb.com/static/images/icons/koyeb.svg" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Koyeb Serverless Platform</h3>
  <p align="center">
    Deploy LlamaIndex on Koyeb
    <br />
    <a href="https://koyeb.com">Learn more about Koyeb</a>
    ·
    <a href="https://koyeb.com/docs">Explore the documentation</a>
    ·
    <a href="https://koyeb.com/tutorials">Discover our tutorials</a>
  </p>
</div>


## About Koyeb and the LlamaIndex example application

Koyeb is a developer-friendly serverless platform to deploy apps globally. No-ops, servers, or infrastructure management.

This repository contains is designed to show how [LlamaIndex](https://www.llamaindex.ai/) applications can be deployed to Koyeb.  The `Dockerfile` in this repository builds an image that serves a LlamaIndex application with a [Streamlit]( https://streamlit.io/) frontend that queries the OpenAI API about the short story "The Gift of the Magi" by O. Henry.

## Getting Started

Follow the steps below to deploy the LlamaIndex application to your Koyeb account.

### Requirements

To use this repository, you need:

* A Koyeb account to build the Docker image and run the Dockerized application.  If you don't already have an account, you can [sign-up for free](https://app.koyeb.com/auth/signup).
* An [OpenAI](https://openai.com/) API key so that our application can send queries to OpenAI.

### Deploy using the Koyeb button

The fastest way to deploy the LlamaIndex application is to click the **Deploy to Koyeb** button below.

[![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?name=example-llamaindex&type=git&repository=koyeb%2Fexample-llamaindex&branch=main&instance_type=micro&builder=dockerfile&env%5BOPENAI_API_KEY%5D=CHANGE_ME&ports=8000%3Bhttp%3B%2F)

Clicking on this button brings you to the Koyeb App creation page with most of the settings pre-configured to launch this application.  You will need to replace the value for the following variable:

* `OPENAI_API_KEY`: Set to your OpenAI API key.

_To modify this application example, you will need to fork this repository. Checkout the [fork and deploy](#fork-and-deploy-to-koyeb) instructions._

### Fork and deploy to Koyeb

If you want to customize and enhance this application, you need to fork this repository.

If you used the **Deploy to Koyeb** button, you can simply link your service to your forked repository to be able to push changes.  Alternatively, you can manually create the application as described below.

On the [Koyeb Control Panel](https://app.koyeb.com/), on the **Overview** tab, click the **Create Web Service** button to begin.

1. Select **GitHub** as the deployment method.
2. Choose the repository containing your application code.
3. In the **Builder** section, select **Dockerfile**.
4. Expand the **Environment variables** section and click **Add Variable** to configure a new environment variable.  Create a variable called `OPENAI_API_KEY`.  Select the **Secret** type and choose **Create secret** in the value.  In the form that appears, create a new secret containing your OpenAI API key.
5. Choose a name for your App and Service, for example `example-llamaindex`, and click **Deploy**.

A container image for the LlamaIndex application will be built and a container will be deployed to Koyeb.  You can follow the build process as the repository is cloned, built, and deployed.  Once the deployment is complete, it will be accessible using the Koyeb subdomain for your service.

## Contributing

If you have any questions, ideas or suggestions regarding this application sample, feel free to open an [issue](//github.com/koyeb/example-llamaindex/issues) or fork this repository and open a [pull request](//github.com/koyeb/example-llamaindex/pulls).

## Contact

[Koyeb](https://www.koyeb.com) - [@gokoyeb](https://twitter.com/gokoyeb) - [Slack](http://slack.koyeb.com/)
