### The Story

This is a very simple Alexa skill.  It is a quiz to test your knowledge of world's capitals and countries.  It suits children and adults alike.  It is a fun game for families and friends.

This game is very easy to play.  It will ask you a set of 5 questions about capitals and countries.  It will go like this:

>You: Alexa, play Capitals and Countries.

>Alexa: There is no game in progress. Do you want to start a new game?

>You: Yes

>Alexa: Capitals and Countries. I will ask you 5 questions, try to get as many right as you can. Just say the number of the answer. Let''s begin. Question 1. Bogota is the capital of which country? 1. Russia. 2. Canada. 3. Thailand. 4. Colombia.

>You: four

>Alexa: That answer is correct. Your score is 1. Question 2. London is the capital of which country? 1. Spain. 2. Turkey. 3. Cuba. 4. United Kingdom.

>You: four

>Alexa: That answer is correct. Your score is 2. Question 3. Baghdad is the capital of which country? 1. Iraq. 2. India. 3. Cuba. 4. Spain.

>You: three

>Alexa: That answer is wrong. The correct answer is 1: Iraq. Your score is 2. Question 4. Vienna is the capital of which country? 1. Thailand. 2. Austria. 3. United Kingdom. 4. Belgium.

>You: two

>Alexa: That answer is correct. Your score is 3. Question 5. Havana is the capital of which country? 1. Egypt. 2. Iraq. 3. Sweden. 4. Cuba.

>You: four

>Alexa: That answer is correct. You got 4 out of 5 questions correct. Thank you for playing!



### Things used in This Project

#### Software and services

Alexa Skill Kit

Amazon Web Services AWS Lambda



### How it was made

Assuming that you already have a developer account, follow theses steps to build this custom skill.


#### Code a AWS lambda function for the skill


1. Select Lambda from Compute service after login to [Console](https://aws.amazon.com/).  If you do not have an account, you can create an AWS account.

2. Skip __Select Blueprint__.

3. In __Configure Function__, enter __Name/Description/Runtime__.

4. Select the __Code Entry Type__ as __Edit Code inline__ and copy/paste the Lambda function from code section below.  Remember to change the App Id.

5. Set the handler and role as follows: (a) keep handler as __index.handler__ and (b) add a new role for __lambda_basic_execution__.

6. You will be asked to setup your IAM role if you have not done so.

7. Keep the advanced setting as default.

8. Select __Next__ and review.  Then __Create Your Function__.

9. Next create an Event Source.  Select __Add event source__ and Select type as __Alexa Skills Set__.

10. Copy the __ARN__ for your lambda function.  You will need it for setting up your skill.

![AWS lambda function](https://hackster.imgix.net/uploads/image/file/142010/create_lambda_function.PNG?w=1280&h=960&fit=max)


#### Setup up skill in Developer Portal

Sign into [Developer Portal](https://developer.amazon.com/) account and select __Alexa__ link.

Click the __Get Started__ below the __Alexa Skills Kit__.


![Alex Get Started](https://raw.githubusercontent.com/pluralsight/guides/master/images/85035b34-0a74-41dc-94d8-d368c30287f0.PNG)


Select __Add a New Skill__.


![description](https://raw.githubusercontent.com/pluralsight/guides/master/images/ff9c6f40-f27d-48c1-ae35-41852aead92e.PNG)


leave the __Skill Type__ as __Custom Interaction Model__.  Add __Name__ and __Innovation Name__.  Select __Save__ and __Next__.


![Create a New Alexa Skill](https://hackster.imgix.net/uploads/image/file/142012/create_new_alexa_skill.PNG?w=1280&h=960&fit=max)


Define skill's interaction model.  Cut & Paste the Intent Schema from code section below.

Add Slot Type as screenshot below.


![Edit Slot Type](https://hackster.imgix.net/uploads/image/file/142011/slot_type.PNG?w=1280&h=960&fit=max)


Add the Utterances.  

Select Save and it should look like screenshot below.


![](https://hackster.imgix.net/uploads/image/file/142013/interaction_model.PNG?w=1280&h=960&fit=max)


In the Configuration tab, add ARN endpoint from the Lambda function and select "No" for the account linking.  Then select Next.


![description](https://raw.githubusercontent.com/pluralsight/guides/master/images/ac70f505-0f40-42ba-9905-e4c4ba3fee7d.PNG)


#### Testing the Capitals and Countries skill

In the Test tab, enter Utterance "Alexa, play Capitals and Countries" and press "Ask Capitals and Countries" button, as shown in screenshot below.

![](https://hackster.imgix.net/uploads/image/file/142015/test_start_play.PNG?w=1280&h=960&fit=max)



Press Listen to listen to quiz question #1.

![](https://hackster.imgix.net/uploads/image/file/142016/test_press_listen.PNG?w=1280&h=960&fit=max)


Enter "three" and press "Ask Capitals and Countries" button.  Then press Listen to listen to Alexa's response to find if you answered correctly.  

![](https://hackster.imgix.net/uploads/image/file/142017/test_answer_1.PNG?w=1280&h=960&fit=max)

And Alexa will ask you the next quiz question.  The quiz will end when you have answered 5 questions.


#### Publishing the Skill







#### Voice Interface Diagram












Or load the live markdown tutorial to check the syntax.

this is a test 

will add more later
