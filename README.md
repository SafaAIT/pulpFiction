# ProjetAI

# Story Generator basé sur la méthode de Lester Dent

Ce projet est un générateur d'histoires basé sur la méthode de Lester Dent, un célèbre auteur de fiction de type "pulp". Il utilise des modèles de langage puissants pour générer des histoires de manière dynamique en suivant une structure narrative spécifique.

## Description

Le générateur utilise un modèle de langage entraîné pour produire une histoire en quatre parties, selon le **Lester Dent Pulp Paper Master Fiction Plot Formula**. Cette formule divise l'histoire en quatre quarts :

1. **Introduction** - Introduction du héros, du conflit principal, et du cadre de l’histoire.
2. **Deuxième quart** - Les conflits et obstacles s'intensifient.
3. **Troisième quart** - Le héros rencontre de nouveaux défis et se rapproche du climax.
4. **Quatrième quart** - Résolution du conflit et conclusion de l'histoire.

Le projet utilise des bibliothèques Python comme `LangChain`, `Transformers`, et `Gradio` pour créer une interface utilisateur permettant de générer une histoire complète basée sur cette structure.

## Prérequis

Avant de commencer, vous devez installer les dépendances suivantes :

```bash
pip install -q -U langchain transformers bitsandbytes accelerate gradio
pip install langchain-community langchain-core

Lester Dent Pulp Paper Master Fiction Plot Story Generator
Description
This project implements a Story Generator based on the Lester Dent Pulp Paper Master Fiction Plot Formula, a structured writing guide used for generating action-packed, pulp fiction stories. The generator leverages advanced machine learning models and the LangChain library for managing interactions between multiple language models (LLMs). The interface is powered by Gradio, enabling easy user input and output for generating a full story.

The generator is broken down into four quarters of the story, and each quarter is created using separate prompts and models to ensure that the story follows the plot formula while maintaining coherence and engagement.

Requirements
Python Libraries
To install the necessary dependencies, use the following command:

bash
Copier
Modifier
pip install -q -U langchain transformers bitsandbytes accelerate gradio langchain-community langchain-core
You will also need to install HuggingFace's transformers library, which provides access to various pre-trained language models.

bash
Copier
Modifier
pip install huggingface-hub
Setting Up HuggingFace Account
To use the pre-trained models, you will need to authenticate using your HuggingFace account.

Go to HuggingFace and create an account.

Log in to your HuggingFace account via the notebook using the following command:

python
Copier
Modifier
from huggingface_hub import notebook_login
notebook_login()
Features
Story Generation: Users can input their own hero, villain, sidekick, victim, and witness, and the system will generate a story based on the Lester Dent formula.

Quartered Story Structure: The story is split into four quarters (introduction, conflict escalation, turning point, and resolution), with each part generated by different models.

Gradio Interface: The user-friendly interface allows users to interactively generate each part of the story and view the results in real-time.

How It Works
The system is divided into several key steps:

Model Loading: The Mistral-7B-Instruct-v0.3 model is used for text generation. This model is loaded with quantization for better performance.

Story Generation Process:

First Quarter: The user provides the basic character details (hero, villain, sidekick, victim, witness), and the first part of the story is generated based on the Lester Dent formula.

Second Quarter: The first part is passed to the model to generate the next segment of the story, escalating the conflict.

Third Quarter: The first and second parts are used to generate the third quarter, where the hero faces greater adversity.

Fourth Quarter: The final quarter is generated, resolving the plot and concluding the story.

Gradio Interface: The interface allows the user to interactively input values for each character and part of the story, and generate the story step-by-step or in its entirety.

Code Breakdown
Quantization: The model uses 4-bit quantization for efficient performance, especially on GPU.

Custom Stopping Criteria: Custom stopping criteria are used to control when the story generation should stop based on specific token patterns (e.g., when a new chapter begins).

Multiple Models: The story generation is divided into multiple stages, each using the same model but different prompts, ensuring that the story follows the established plot structure.

Interface
Once the program is running, the user can interact with the Gradio interface. The key features of the interface are:

Textboxes for Input: Users can provide details about the characters (hero, villain, sidekick, victim, and witness).

Buttons to Generate Parts: Buttons allow users to generate each part of the story (first, second, third, and fourth quarters).

Textboxes for Output: The generated story parts will be displayed in textboxes where the user can view and modify them.

Generate Full Story: Once all parts have been generated, users can click on the "Generate Full Story" button to combine all parts into one continuous narrative.



## Getting started

To make it easy for you to get started with GitLab, here's a list of recommended next steps.

Already a pro? Just edit this README.md and make it your own. Want to make it easy? [Use the template at the bottom](#editing-this-readme)!

## Add your files

- [ ] [Create](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#create-a-file) or [upload](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#upload-a-file) files
- [ ] [Add files using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html#add-a-file-using-the-command-line) or push an existing Git repository with the following command:

```
cd existing_repo
git remote add origin https://git.enib.fr/s1aitlam/projetai.git
git branch -M main
git push -uf origin main
```

## Integrate with your tools

- [ ] [Set up project integrations](https://git.enib.fr/s1aitlam/projetai/-/settings/integrations)

## Collaborate with your team

- [ ] [Invite team members and collaborators](https://docs.gitlab.com/ee/user/project/members/)
- [ ] [Create a new merge request](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html)
- [ ] [Automatically close issues from merge requests](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html#closing-issues-automatically)
- [ ] [Enable merge request approvals](https://docs.gitlab.com/ee/user/project/merge_requests/approvals/)
- [ ] [Set auto-merge](https://docs.gitlab.com/ee/user/project/merge_requests/merge_when_pipeline_succeeds.html)

## Test and Deploy

Use the built-in continuous integration in GitLab.

- [ ] [Get started with GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html)
- [ ] [Analyze your code for known vulnerabilities with Static Application Security Testing (SAST)](https://docs.gitlab.com/ee/user/application_security/sast/)
- [ ] [Deploy to Kubernetes, Amazon EC2, or Amazon ECS using Auto Deploy](https://docs.gitlab.com/ee/topics/autodevops/requirements.html)
- [ ] [Use pull-based deployments for improved Kubernetes management](https://docs.gitlab.com/ee/user/clusters/agent/)
- [ ] [Set up protected environments](https://docs.gitlab.com/ee/ci/environments/protected_environments.html)

***

# Editing this README

When you're ready to make this README your own, just edit this file and use the handy template below (or feel free to structure it however you want - this is just a starting point!). Thanks to [makeareadme.com](https://www.makeareadme.com/) for this template.

## Suggestions for a good README

Every project is different, so consider which of these sections apply to yours. The sections used in the template are suggestions for most open source projects. Also keep in mind that while a README can be too long and detailed, too long is better than too short. If you think your README is too long, consider utilizing another form of documentation rather than cutting out information.

## Name
Choose a self-explaining name for your project.

## Description
Let people know what your project can do specifically. Provide context and add a link to any reference visitors might be unfamiliar with. A list of Features or a Background subsection can also be added here. If there are alternatives to your project, this is a good place to list differentiating factors.

## Badges
On some READMEs, you may see small images that convey metadata, such as whether or not all the tests are passing for the project. You can use Shields to add some to your README. Many services also have instructions for adding a badge.

## Visuals
Depending on what you are making, it can be a good idea to include screenshots or even a video (you'll frequently see GIFs rather than actual videos). Tools like ttygif can help, but check out Asciinema for a more sophisticated method.

## Installation
Within a particular ecosystem, there may be a common way of installing things, such as using Yarn, NuGet, or Homebrew. However, consider the possibility that whoever is reading your README is a novice and would like more guidance. Listing specific steps helps remove ambiguity and gets people to using your project as quickly as possible. If it only runs in a specific context like a particular programming language version or operating system or has dependencies that have to be installed manually, also add a Requirements subsection.

## Usage
Use examples liberally, and show the expected output if you can. It's helpful to have inline the smallest example of usage that you can demonstrate, while providing links to more sophisticated examples if they are too long to reasonably include in the README.

## Support
Tell people where they can go to for help. It can be any combination of an issue tracker, a chat room, an email address, etc.

## Roadmap
If you have ideas for releases in the future, it is a good idea to list them in the README.

## Contributing
State if you are open to contributions and what your requirements are for accepting them.

For people who want to make changes to your project, it's helpful to have some documentation on how to get started. Perhaps there is a script that they should run or some environment variables that they need to set. Make these steps explicit. These instructions could also be useful to your future self.

You can also document commands to lint the code or run tests. These steps help to ensure high code quality and reduce the likelihood that the changes inadvertently break something. Having instructions for running tests is especially helpful if it requires external setup, such as starting a Selenium server for testing in a browser.

## Authors and acknowledgment
Show your appreciation to those who have contributed to the project.

## License
For open source projects, say how it is licensed.

## Project status
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.
