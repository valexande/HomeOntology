# HomeOntology
The framework for the paper send to ESWC 20.

Title:

Authors: Alexandros Vassiliades, Nick Bassiliades, Filippos Gouidis, and Theodore Patkos

Abstract:
In the field of domestic robotics, which can perform human scaled tasks, having a rich knowledge representation is a fundamental aspect
that offers exibility and scalability to the system. More importantly for the system is to have capabilities which use semantic information, such as which household objects are related between them with respect to a human scaled action. In this paper, we propose a general purpose ontology which recommends sequence of actions on how to perform human scaled tasks in a dynamic environment, answer semantically related questions about household objects, and use Semantic Web technologies to find semantically related entities from the web ontologies DBpedia, ConceptNet, and WordNet, with the ones existing in the local Knowledge Base. This ontology tackles to a point the need of logic rules that semantically connect objects. Allows for more complex questions to be addressed to the system. It potentially, offers to systems the ability of performing mere complex tasks. The ontology information and schema was inspired by the VirtualHome dataset. The framework was evaluated via crowd source evaluation.

We are giving two different editions of our framework. In the first one, Household_Ontology the framework search in all ConceptNet, WordNet, and DBpedia to return results. In the second one Household_Ontology_Restricted_to_House_Objects the framework is restricted to return only objects found in a domestic environment.

The main class of our project is the Ontology_Main. Therefore, the framework initializes from there. After that the user is faced with the choices:



Hello! :) Right Now the questions that I can answer for you are:

(1) How you can perform a specific task. Press 1 then give the task or tasks that you want to perform.
(2) What can you do with some objects. Press 2 then give the objects
(3) What other objects are related to some objects. Press 3 then give me the objects
(4) On what objects can you perform an action. Press 4 then the action or actions.
(5) On what object you can perform an action with a condition. Press 5 then give me action and condition.
(6) What actions can be performed on a set of objects. Press 6 then give me objects.
(7) What sequence of actions can be performed on a single object. Press 7 then give me object.
(8) Return sequence of action of specific instance. Press 8 then give me instance.
(9) Return the sequences of actions, based on some objects order. Press 9 then give the objects you want to search for in specific order.
(10) You can create your own query. Press 10.
(11) If you want some general Web Knowledge about an entity. Press 11

The user must then pick up a choice and start following the instructions of the framework, as for the input data needed in order for the framework to return the desirred answer. 


(1) Example:

Choice 3 

Give me the objects for which you want me to find other objects! If there are more than one seperate them by comma :)
coffee, milk      ##The format for every question must be like this 


[coffee1, coffee2]

Which coffee do you prefer? Give me the number in the list

1


[milk1 ]

Which milk do you prefer? Give me the number in the list

1


[coffee1, milk1 ]

['kitchen1 ', 'coffe_maker1 ', 'coffee_filter1 ', 'ground_coffee1 ', 'water1 ', 'coffee_pot1 ', 'coffee_cup1 ', 'food_sugar1 ', 'spoon1 ', 'coffee_cup4 ', 'coffee_table1 ', 'coffee_cup2 ', 'glass1 ', 'ice1 ', 'table1 ', 'stove1 ']


(2) Example with Object Not in the KB:

Choice 2

Give me the objects for which you want me to find sequence of actions! If there are more than one seperate them by comma :)

cappuccino, milk

Sorry but I do not have in my KB the entity cappuccino do you want me to search on the web for it?

Tell me [y/n], y = yes || n = no

y

I have found similarities with the ones below
 
Cappuccino is IsA drink, beverage. 

Cappuccino is RelatedTo coffee, espresso, steam, caffe_latte, italy, foam. 

Similar objects that I have in my KB are the following. Please give a number in the list to answer your query

['coffee', 'coffee2 ', 'coffee pot', 'coffee cup', 'coffee cup4 ', 'coffee cup2 ', 'coffee pot3 ', 'coffee pot2 ', 'coffee table', 'coffee table2 ', 'ground coffee', 'coffee filter']

1

coffee1 

['milk1 ']

Which milk do you prefer? Give me the number in the list

1

['coffee1 ', 'milk1 ']

['make_iced_coffee1580 ', 'make_coffee403 ', 'make_coffee1418 ', 'make_coffee171 ']

(3) Example Action Not existing in the KB:

4

Give me the actions you want me to search for! If there are more than one seperate them by comma :)

looking

For looking I have to recommend

['lookat', 'cut', 'stretch', 'text']

Do you want any, if Yes give a number of the list you see

1

['lookat']

['hanger1 ', 'computer1 ', 'laptop1 ', 'coffee_pot1 ', 'cat1 ', 'table1 ', 'woman2 ', 'bed1 ', 'cellphone1 ', 'child1 ', 'document1 ', 'stove1 ', 'soap1 ', 'child2 ', 'notes1 ', 'cards1 ', 'mirror1 ', 'television1 ', 'bookshelf1 ', 'chair1 ', 'man1 ', 'woman1 ', 'phone1 ', 'dog1 ', 'food_food1 ', 'coffee_table1 ', 'keyboard1 ', 'toothbrush_holder1 ', 'picture2 ', 'face1 ', 'electrical_outlet1 ', 'sink1 ', 'address_book1 ', 'clothes_pants1 ', 'painting1 ', 'book1 ', 'wall_clock1 ', 'bills1 ', 'towel1 ', 'dresser1 ', 'drawing1 ', 'desk1 ', 'plate3 ', 'kitchen_counter1 ', 'fridge1 ', 'crackers1 ', 'lamp1 ', 'magazine5 ', 'remote_control1 ', 'light1 ', 'paper1 ', 'water1 ', 'pot1 ', 'vacuum_cleaner1 ', 'paper_towel1 ', 'table_cloth1 ', 'pillow1 ', 'shoes1 ', 'clothes_underwear2 ', 'dvd_player1 ', 'homework1 ', 'food_dessert1 ', 'closet1 ', 'brush1 ', 'toy1 ', 'magazine3 ', 'cd_player1 ', 'groceries1 ', 'light2 ', 'food_bread1 ', 'telephone1 ', 'painting3 ', 'spoon1 ', 'cookingpot1 ', 'faucet1 ', 'painting2 ', 'plate4 ', 'cup4 ', 'window1 ', 'sofa1 ', 'bowl1 ', 'toilet1 ', 'clothes_dress1 ', 'creditcard1 ', 'notebook1 ', 'food_cheese1 ', 'sponge1 ', 'glass1 ', 'plate1 ', 'lightswitch1 ', 'towel2 ', 'dishrack1 ', 'teeth1 ', 'cabinet1 ', 'hair1 ', 'fly1 ', 'kitchen_cabinet1 ', 'cleaning_bottle1 ', 'board_game1 ', 'magazine2 ', 'newspaper1 ', 'hands_both1 ', 'drinking_glass1 ', 'food_food2 ', 'receipt1 ', 'lighting1 ', 'washing_machine1 ', 'clothes_shirt1 ', 'coffe_maker1 ', 'mop1 ', 'clothes_pants2 ', 'magazine1 ', 'toaster1 ', 'cat2 ', 'cup1 ', 'dry_pasta1 ', 'bathtub1 ', 'couch1 ', 'razor1 ', 'food_cheese2 ', 'arms_both1 ', 'picture1 ', 'clothes_shirt3 ', 'clothes_shirt2 ', 'paper2 ', 'alarm_clock1 ', 'light3 ', 'water_glass1 ', 'basket_for_clothes1 ', 'centerpiece1 ', 'toilet_paper1 ', 'wall1 ', 'stereo1 ', 'shower1 ', 'toothbrush1 ', 'folder2 ', 'radio1 ', 'magazine4 ', 'food_vegetable1 ', 'blanket1 ', 'feet_both1 ', 'folder1 ', 'homework2 ', 'shampoo1 ', 'coffee1 ', 'button1 ', 'food_noodles1 ', 'duster1 ', 'man2 ', 'milk1 ', 'printer1 ', 'rag1 ']

 
