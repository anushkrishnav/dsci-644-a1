# Task 1: Introduction to Kaggle, Kaggle Dataset, and GitHub's GraphQL API

In this task, you will gain insights into Kaggle, Kaggle datasets, and GitHub's GraphQL API, all of which are essential for our data extraction. This task will also help you obtain your kaggle and GitHub token.

<!-- 🔗 **Click through the demo** to familiarize yourself with the steps required: [Task 1 Demo](https://app.supademo.com/embed/7EtskutdCC93mvxG_ZEdV) -->

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
5. Move the `kaggle.json` file from your Downloads folder to Task_1 folder.
6. Add this file to your `.gitignore` file. Remember, you should never commit API keys to GitHub.


### Step 3: Obtain the Kaggle repo_list Dataset
1. Follow the instructions in the [Python Notebook](/Tasks/Task_1/task_1.ipynb)] to obtain the `repo_list` dataset.
2. Upload the extracted CSV to MyCourses.


## Part 2: GitHub's GraphQL API

<!-- 🔗 **Click through the demo** to learn more about GitHub's GraphQL API: [GitHub's GraphQL API Demo](https://app.supademo.com/embed/Suz5pnDrt_pFS81gg5vM4) -->

### Step 1: Create a GitHub Account

1. Go to [GitHub](https://github.com/).
2. Sign up for a GitHub account if you don't already have one.

### Step 2: Obtain the GitHub API Token

1. Log in to your GitHub account.
2. Go to your account settings.
3. Navigate to the Developer Settings.
4. Generate a fine-grained API token.
5. Keep this token secure.
6. Its recommended to store and use this token from a `.env` file. Remember, you should never commit API keys to GitHub.

### Step 3: Use the GitHub API Token

1. Use the GitHub API token to call the GitHub GraphQL server.
2. The GraphQL query file required to obtain the data will be provided.
3. Check the `Task_1` folder for the GraphQL query file.

### Step 4: Obtain the GitHub repo_list and the subsequent Issues data from the GraphQL API
1. Open the [Python Notebook](/Tasks/Task_1/task_1.ipynb) to proceed with the task. 
2. Follow the instructions in the notebook to obtain the `repo_list` and the subsequent `Issues` data from the GraphQL API.
3. Upload the extracted JSON files to MyCourses.

If you are new to GraphQL, you can learn more about it [here](https://graphql.org/).

🎉 If you have completed all the steps, Congratulations! You have successfully completed Task 1. 🎉

### Additional Resources to learn about graphQL and GitHub's GraphQL API

- [GraphQL](https://graphql.org/)
- [GitHub GraphQL API](https://docs.github.com/en/graphql)
- [Github GraphQL API Explorer](https://docs.github.com/en/graphql/overview/explorer)
- [GraphQL vs REST](https://www.apollographql.com/blog/graphql-vs-rest-5d425123e34b/)
- [Learn more about GraphQL](https://youtu.be/ZQL7tL2S0oQ?si=QRfxcGmzmxvBQ0_5)



[![task-button]][Shield]
<!-----------BUTTON----------------------------------------------------------------->

[task-button]: https://img.shields.io/badge/Let's_jump_to_task_2-F76902?style=for-the-badge

[Shield]: ../Task_2/task_2.md
