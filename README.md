# Ontology_Unity
Integration of an Ontology reasoner in Unity.

### Prerequisites

Unity Game Engine: https://unity3d.com/get-unity/download

* Install Unity
* Create a new Unity 2D/3D project
* Import Ontology_Unity_Package.unitypackage

### Getting started

* Copy your .owl file to folder Assets/OntologyModule/encodings/
* In file Assets/OntologyModule/encodings/main.bvr, do the following: 
  * Make sure that relativePath="ontology.owl" is your ontology name. 
* In file Assets/OntologyModule/OntologyWebservice.cs, do the following:
  * Change 'project_key' to your project key
  * Change 'ontology_file_name' to your owl file name, or rename your owl file to 'ontology.owl'

### Start your project

* In file Assets/OntologyModule/encodings/main.bvr, do the following: 
  * Take a look at how example rules are defined to print the results of the OWL inferencing
  * Define the rules you need for your ontology
* In Unity, create a new GameObject
* In Unity, add the script Assets/OntologyModule/OntologyWebservice.cs to a GameObject
* Check output from the reasoner in the Unity Console
* In the script Assets/OntologyModule/OntologyWebservice.cs
  * Parse the text response from the ontology reasoner
  * Define an approrpiate data structure for the response
  * Do application specific operations

### Authors

* Andreas Brännström {andreasb@cs.umu.se} [Homepage](https://people.cs.umu.se/andreasb/)

Department of Computing Science  
Umeå university  
SE-901 87, Umeå, Sweden  
