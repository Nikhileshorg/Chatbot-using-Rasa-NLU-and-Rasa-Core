
#### Training the NLU model ####

``` python nlu_model.py ```

#### Training the Rasa Core model ####

The biggest change in how Rasa Core model works is that custom action 'action_weather' now needs to run on a separate server. That server has to be configured in a 'endpoints.yml' file.  This is how to train and run the dialogue management model:  
1. Start the custom action server by running:  

``` python -m rasa_core_sdk.endpoint --actions actions ```  

2. Open a new terminal and train the Rasa Core model by running:  

``` python dialogue_management_model.py```  
 
3. Talk to the chatbot once it's loaded.  

#### Starting the interactive training session ####

The process of running the interactive session is very similar to training the Rasa Core model:
1. Make sure the custom actions server is running:  

``` python -m rasa_core_sdk.endpoint --actions actions ```  

2. Start the interactive training session by running:  

``` python train_interactive.py ```  

#### Connecting a chatbot to Slack ####
1. Configure the slack app as shown in the video  
2. Make sure custom actions server is running  
3. Start the agent by running run_app.py file (don't forget to provide the slack_token)  
4. Start the ngrok on the port 5004  
5. Provide the url: https://your_ngrok_url/webhooks/slack/webhook to 'Event Subscriptions' page of the slack configuration.  
6. Talk to you bot.  








