# HomeOntology

Title: A Semantic Question Answering Framework about Household Objects and Actions

Authors: Alexandros Vassiliades, Nick Bassiliades, Filippos Gouidis, and Theodore Patkos

Abstract:
In the field of domestic robotics, having a rich representationof knowledge offers flexibility to the robotic platform. It is important forthe  robotic  platform  to  have  capabilities  that  use  semantic  knowledgeabout how household objects are related to each other and with respectto human actions. In this paper, we present a domain dependent frame-work for household environments which was constructed by extractingconcepts and knowledge from the VirtualHome dataset. The frameworkrecommends sequences of actions on how to perform human scaled tasksin  a  household  environment,  answers  questions  about  semantically  re-lated household objects, and performs semantic matching between enti-ties from the web knowledge bases DBpedia, ConceptNet, and WordNet,with the ones existing in the local Knowledge Base. We offer a set of pre-defined SPARQL templates that directly address the ontology on whichour framework is built, and querying capabilities through SPARQL. Weevaluated our framework via two different user evaluations.

We are giving two different editions of our framework: 

(i) In the first one, Household_Ontology the framework search in all ConceptNet, WordNet, and DBpedia to return results. 

(ii) In the second one Household_Ontology_Restricted_to_House_Objects the framework is restricted to return only objects found in a domestic environment.

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


Example:

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


An issue that might occur, the jar file are the ones that are sending SPARQL queries to the Ontology. The reason we use Java although all the framework is built with Python is because Python libraries could not parse the ontology quickly enough. Therefore, in order for the jar file to be functional, one may need to take the java code (inside the zip files), change the path to the .ttl file, create a jar. After that you are ready to go :).

We need to apologize for the last part, but unfortunately python does not have an rdf parser for large files that has good time performance. Thus, we used java only for this part.
