# Ontology Unity Package
* Integration of an Ontology reasoner in Unity through a web API. 
* The Ontology Unity Package comes with a set of helper functions in C# to do operations with ontologies in Unity.
* This allows Unity-ontology projects to be deployed on any device that has internet access.

### The integrated Ontology reasoner (not required to install)

* Ontology reasoner: BaseVISor
* BaseVISor 2.0.2 is licensed for academic and research use free of charge; all other uses require a commercial license.
* Supported syntaxes: RDF/XML, OWL/XML, All OWL API
* Supported reasoning services: realisation, classification, satisfiability, conjunctive query answering, entailment, consistency.
* Creators of BaseVISor: VIStology, Inc.
* More info: https://www.vistology.com/products/

### Prerequisites of the Ontology Unity Package

Unity Game Engine: https://unity3d.com/get-unity/download

* Install Unity
* Create a new Unity 2D/3D project
* Import Ontology_Unity_Package.unitypackage

### Getting started with the Ontology Unity Package

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

### Authors of the Ontology Unity Package

* Andreas Brännström {andreasb@cs.umu.se} [Homepage](https://people.cs.umu.se/andreasb/)

Department of Computing Science  
Umeå university  
SE-901 87, Umeå, Sweden  
