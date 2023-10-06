Setting up jenkins:
1. install and congifure jenkins on your server. Ensure jenkins is running
2. Access the jenkins dashborad using your browser.
3. Create a new jenkins job for your project.
4. Add the github URL of this project in the source code management section.
5. Select "GitHub hook trigger for GITScm polling" in Build Triggers section.
6. Now add the build steps to start the container and save the project.

Setting up Github:
1. Go to the setting of this project and in the webhook section click on Add webhooks.
2. Go to payload URL, add the public ID address with the port on which you are accessing jenkins and github-webhook
3. It will look like this (eg. 'https://2.2.2.2:8080/github-webhook')
4. select the event like "just the push event" in the next option and click on "Add-webhook"
5. Now, make any changes in this project and commit them.

In jenkins, check that one build will be after you commit. So, github webhooks are used to trigger a build in jenkins whenever someone commits to the project.


