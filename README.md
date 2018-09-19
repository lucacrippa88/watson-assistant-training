# Creation and training of a Virtual Assistant with Watson Assistant

Watson Assistant training via web interface on IBM Cloud. In this repository I will put examples of how to create and train a Chatbot using Watson Assistant service.


## Prerequisites

In order to use this code, it's necessary to have:

1. An IBM Cloud account. It's free of charge, no credit card required (only a valid email address)
2. A Watson Assistant Lite Service (free of charge)


## How to train Watson Assistant

In order to perform the Watson Assistant training, the trainer should use the following features, named Intents and Entities, with the related catalogues.

### Intents

When the user writes something to a general Chatbot, he has in mind a precise intent for each sentence: if the context of the conversation is a restaurant, a sentence "I'm really hungry" could have the intent "I want to order some food". Most of the Chatbots available in the Internet work by keyword: i.e. if a user writes "I'm not really hungry by now" and the keyword is only "hungry", the Chatbot could interpret this as "Place a food order", even if in this case the intent of the user is not to place a food order.
With Watson Assistant, powered by IBM Watson Machine Learning algorithms, you can actually train the Chatbot to recognize the real intent of the user by providing a set of typical sentences as a knowledge base on that intent: as the user writes a sentence to the Chatbot, the algorithm performs an analysis of the sentence, understanding it by a correlation of it's knowledge base.
With Watson Assistant you can create your own intents with your own knowledge base, either by using the graphic interface or by uploading a set of sentences in a well structured csv file.

#### Content Catalog

Watson Assistant has a set of intents ready to be used, divided by categories.

### Entities

Entities are used to enhance the conversation capabilities. The best way to understand entities could be the following: let's create an intent for "food order", that understands sentences from "can I place a food order" to "I'm really hungry...". Let's say that a restaurant menu is full of options: so instead of creating one intent for each menu entry, we can create only one intent for a general "food order", and then we can use entities to specify what kind of food we are about to order. So if the user will say "I'd like to order two margherita pizzas", Watson Assistant will identify:
1. intent: #food_order
2. entity: @number:2
3. entity: @pizza:margherita

#### System Entities

The system entities are similar to the Intents Content Catalog, as they are a bunch of ready to use entities: number, percentage, currency, date, time, etc.


## Create a Dialog

The Dialog is a set of nodes, activated when one or more conditions occur, that contain the conversation flow. the nodes are evaluated from the top to the bottom.

### Some important nodes

#### First node: welcome
The welcome node is called when the convresation starts. It promps the user with a "welcome" sentence as he starts the chatbot. This node should be always the first node in the dialog.

#### Last node: anything_else
The anything_else node is entered when the chatbot doesn't find a correlation between the user's sentence and a intent. This node should be always the last node in the dialog.


## How to enhance Watson Assistant conversations

The basic features explored in the previous paragraphs allowed to create a simple chatbot understanding and answering our questions.

### Context variables

To be updated.

### Slots

Slots are the simplest way to collect information from user inputs. Just activate slots, add as many as you need, and store contents into Context Variables. If a prompt question is added, the slot becomes required; elsewhere, is optional.

### Digressions

To be updated.

### Fuzzy Matching on Entities

Fuzzy Matching (beta) is a feature that enables the automatic correction / interpretation of the Entities, considering typos / keyboard errors / user errors.
For example, if an user writes "Pizza maghrerita" (with typo errors), with Fuzzy matching enabled Watson Assistant can understand the Entity as "Pizza margherita".
In some cases, Fuzzy Matching needs to be disabled: for example, if the user must insert a name, surname or a banking code, Watson Assistant should not try to interpretate the user input, risking to make errors.

## Tutorials

Please find tutorials on how to train Watson Assistant here: link to come (Italian spoken, but with English interface).

1. Riconoscere gli Intenti: https://www.youtube.com/watch?v=imEN7GtX5zw&t=1s
2. Gli Intenti generali: https://www.youtube.com/watch?v=isrVffJ1po8
3. Le Entità: https://www.youtube.com/watch?v=rNoa4udCGrc
4. Raccogliere informazioni con gli Slot: https://www.youtube.com/watch?v=d3tbYvYz_UU
5. Le Digressioni 1/2: https://www.youtube.com/watch?v=Qa4Y15XzpRc&t=1s
6. Le Digressioni 2/2: https://www.youtube.com/watch?v=okxMSkfbQVM
7. Organizzare Intenti ed Entità: https://www.youtube.com/watch?v=KTkZRF2lLPk
8. Raccogliere informazioni testuali da input: https://www.youtube.com/watch?v=4HMBBB51iZQ
9. Gestire le Variabili di contesto: https://www.youtube.com/watch?v=Z8pujSseWTY
10. Integrazione con altri Servizi: https://www.youtube.com/watch?v=TDMdf15wRW8
11. Controllo e debug: https://www.youtube.com/watch?v=7mp-R_lMLyc
12. More to come...
13. More to come...

Linked video tutorials are not official assets.

Please refer to this Github repository to know how to integrate the Virtual Assistant into a web app:
1. PHP: https://github.com/lucacrippa88/watson-assistant-php
2. Node.js: to be updated

## Disclaimer

This is not an official asset. It has been created by me and it's not intended for professional use. However, it follows all guidelines you can find in https://console.bluemix.net/docs/services/conversation/ and in https://www.ibm.com/watson/developercloud/assistant/api/v1/.
For Watson Services SLAs, please have a look here: https://www-03.ibm.com/software/sla/sladb.nsf/sla/bm-0038-09.
Linked video tutorials are not official assets.

## License

This project uses the Apache License Version 2.0 software license. https://github.com/lucacrippa88/watson-assistant-training/blob/master/LICENSE
