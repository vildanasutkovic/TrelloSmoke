# TrelloSmoke

Pre-requisite: Have Postman installed

Attached are 2 files:
  1. Trello App.postman_collection.json
  2. Trello App.postman_environment.json

# Trello App.postman_collection.json
In this file, there are several smoke tests written for testing the Trello App. Performed smoke tests are: 
  1. Create Board
  2. Create a new List Mobitel
  3. Create a new List Frizider
  4. Create a new Card
  5. Add member to a board
  6. Add member to a card
  7. Move card to another list
  8. Delete a card
  9. Delete a board

Tests are done in this order, so they can be performed logically. Each test is performed by opeing desired file and clicking blue "Send" button in the right-upper corner. The order of making things work is create: board, list, card, members, deletion. All tests are performed successfully.

## Steps
First we create a new Board, in our case named "vildanin board". Then we create 2 lists in the board named "Mobitel" and "Frizider" so that we can manipulate with them later. After that, card named "Laptop" is added to the "Mobitel" list.
We wanted to have more than one member(admin), so we added new member "anidamusinovic" to a board. In the next step we assigned "anidamusinovic" to a "Laptop" card. Then, we moved card "Laptop" with it's user from current list "Mobitel" to another list "Frizider". After, we delete "Laptop" card, and delete board "vildanin board" afterwards.

# Trello App.postman_environment.json
In this file, there are all variables with their values that are used for performed smoke test. Used variables are key, token, board_id, board_name, card_id, list_id_mobitel, list_id_frizider, anidas_id, vildanas_id, card_name. These variables are updated regularly according to the tests performed.

# Running Trello App from terminal using Postman
First, open Command Prompt or Terminal on your device. When it is opened, type "**newman run path_of_collection_file -e path_of_environment_file**" (without quotes), and press Enter. Your line should look something like this 

**newman run /Users/vildana/Desktop/TrelloApp/Trello.App.postman_collection.json  -e /Users/vildana/Desktop/TrelloApp/Trello.App.postman_environment.json**

For obtaining path, if you don't know how to find it, you can just hold click on your .json file, and drag it into terminal and your required path will be shown immediatelly.
