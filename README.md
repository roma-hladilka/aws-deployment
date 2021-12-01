Setup CI/CD with AWS ECS and Github Actions
First step
Follow this guide. Once complete, when your application is deployed, proceed to the next step

Second step
Go to the "Action" tab in your repo, and select "Deploy to Amazon ECS". Please check screens bellow

<img style="transform: scale(0.65)" src="https://user-images.githubusercontent.com/22969597/142990438-7d26783c-32ad-49a8-867a-788dcea99bb0.png">

<img style="transform: scale(0.65)" src="https://user-images.githubusercontent.com/22969597/142990463-65ce2da1-5940-479d-ad6e-1fbacf34b5c3.png">

There please add a new comment without changes, make "git pull" and go to your code. There create please task-definition.json file, in the root directory. After that go to AWS console > ECS > Task Definitions and copy and past info from there to your new file. Please check screen bellow.

<img style="transform: scale(0.65)" src="https://user-images.githubusercontent.com/22969597/142991000-c0b9d1b6-cfce-42d4-b236-ebfed6ff6b1b.png">

Third step
Go to "Setting", and there select "Secrets" in the sidebar. There create a new secrets, which we will use in next step. Here is the list of secrets which you have to create:

    AWS_ACCESS_KEY_ID
    AWS_SECRET_ACCESS_KEY
Fourth step
Go to .github/workflows/***.yml.

Replace all this envs with data which you got by following this guide.

<img style="transform: scale(0.65)" src="https://user-images.githubusercontent.com/22969597/142993672-12df8d5a-6075-43cb-9fee-4cd6d4064dd1.png">

Fifth
Now specify the branch on which the Action should be launched when pushing. By default this is the "master". Please check screen bellow

<img style="transform: scale(0.65)" src="https://user-images.githubusercontent.com/22969597/142996479-021b06c7-d379-4cc0-946e-d359fa3b80ea.png">

Last step
This all, now just push your code to the branch which you specified in previous step.