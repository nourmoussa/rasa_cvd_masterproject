# rasa_cvd_masterproject
**To start the installation run: **
- python3.7 -m pip install virtualenv 
- mkdir rasa-demo
- cd rasa-demo 

#Create a new virtual environment by choosing a Python interpreter and making a ./venv directory to hold it:
python3.7 -m venv ./venv
#activate the virtual environment
source ./venv/bin/activate

#Install Rasa Open Source using pip (requires Python 3.7, or 3.8).
pip3 install -U --user pip && pip3 install rasa
#or 
python3.7 -m pip install rasa 

Commands for rasa: 

- rasa init #Creates a new project with example training data, actions, and config files.
- rasa shell #Loads your trained model and lets you talk to your assistant on the command line.
- rasa train #Trains a model using your NLU data and stories, saves trained model in ./models.
- rasa interactive #Starts an interactive learning session to create new training data by chatting to your assistant.
- rasa run	#Starts a server with your trained model.
- rasa run actions	#Starts an action server using the Rasa SDK.
- rasa visualize	#Generates a visual representation of your stories.
- rasa test	#Tests a trained Rasa model on any files starting with test_.
- rasa data split nlu	#Performs a 80/20 split of your NLU training data.
- rasa data convert	#Converts training data between different formats.
- rasa data migrate	#Migrates 2.0 domain to 3.0 format.
- rasa data validate	#Checks the domain, NLU and conversation data for inconsistencies.
- rasa export	#Exports conversations from a tracker store to an event broker.
- rasa evaluate markers	#Extracts markers from an existing tracker store.
- rasa x	#Launches Rasa X in local mode.
- rasa -h	#Shows all available commands.


Connect to whatsapp using Twilio: 
1. In Terminal 1: 
- activate rasa22
- train model
- rasa run -m models —enable-api —cors”*”

2. In Terminal 2:
- unzip ngrok 
- authtoken xx
- ngrok http 5005

3. In Credentials file:
Add a WhatsApp section with details “authtoken, WhatsApp number and SID” 
twilio: 
  account_sid: "xxxxxxxxxx"
  auth_token: "xxxxxxxxxx"
  twilio_number: "whatsapp:+14155238886" #number taken from twilio account 

4. In twilio sandbox: copy link obtained in the terminal after running "ngrok http 5005" and paste it in the sandbox.

5. Save twilio number on WhatsApp and enter  message “join nervous-this” to activate the chat
