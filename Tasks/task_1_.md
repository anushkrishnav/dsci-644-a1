# Task 1: Introduction to Kaggle, Kaggle Dataset, and GitHub's GraphQL API

In this task, you will gain insights into Kaggle, Kaggle datasets, and GitHub's GraphQL API, all of which are essential for data extraction and automation in our course. We'll walk you through the steps for both Kaggle and GitHub.

🔗 **Click through the demo** to familiarize yourself with the steps required: [Task 1 Demo](https://app.supademo.com/embed/7EtskutdCC93mvxG_ZEdV)

## Part 1: Kaggle

### Kaggle and Kaggle Datasets

[Kaggle](https://www.coursera.org/articles/kaggle) is a platform for data science competitions where participants compete to create the best models for solving specific problems or analyzing certain datasets. The platform is also used for learning, collaboration, job opportunities, community building, and research in the data science and machine learning fields.

**Kaggle Datasets** allows a user to publish and share datasets privately or publicly. Kaggle provides resources for storing and processing datasets, but there are certain technical specifications: 100GB per dataset limit and 100GB max private datasets (if you exceed this, either make your datasets public or delete unused datasets).

Source: [Kaggle Datasets](https://www.kaggle.com/docs/datasets)

### Step 1: Create a Kaggle Account

1. Go to [Kaggle](https://www.kaggle.com/).
2. Sign up for a Kaggle account if you don't already have one.

### Step 2: Obtain the Kaggle API Key

1. Log in to your Kaggle account.
2. Click on your profile picture in the upper right corner and select "Account."
3. Scroll down to the "Settings" section.
4. Click on "Create API Token." This action will download a file named `kaggle.json` to your computer.

### Step 3: Use the Kaggle API Key in Colab

1. Copy the provided Colab file.
2. Upload the `kaggle.json` file to your Colab environment.
3. Use the Kaggle API key in your Colab notebook to access Kaggle datasets and competitions.

### Step 4: Obtain the `repo_list` Dataset

1. Follow the instructions in the Colab file to obtain the `repo_list` dataset.
2. Upload the extracted CSV to MyCourses.

## Part 2: GitHub's GraphQL API

🔗 **Click through the demo** to learn more about GitHub's GraphQL API: [GitHub's GraphQL API Demo](https://app.supademo.com/embed/Suz5pnDrt_pFS81gg5vM4)

### Step 1: Create a GitHub Account

1. Go to [GitHub](https://github.com/).
2. Sign up for a GitHub account if you don't already have one.

### Step 2: Obtain the GitHub API Token

1. Log in to your GitHub account.
2. Go to your account settings.
3. Navigate to the Developer Settings.
4. Generate a fine-grained API token.
5. Keep this token secure.

### Step 3: Use the GitHub API Token

1. Use the GitHub API token to call the GitHub GraphQL server.
2. The GraphQL query file required to obtain the data will be provided.
3. Starter code on Kaggle will be provided as well.

🎉 Congratulations! You've successfully completed Task 1.



[![task-button]][Shield]
<!-----------BUTTON----------------------------------------------------------------->

[task-button]: https://img.shields.io/badge/Let's_jump_to_task_2-F76902?style=for-the-badge

[License]: LICENSE
[Shield]: Tasks/task_2_.md
[KBD]: Types/KBD.md
[#]: #

<!---------------------------------[ Badges ]---------------------------------->
