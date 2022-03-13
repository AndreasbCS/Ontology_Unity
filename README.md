# UnityIIS - Symbolic Reasoning in Unity
UnityIIS (Unity Intelligent Interactive Systems) is a package for the Unity Game Engine for implementing intelligent interactive systems (IIS). In particular, systems that integrates symbolic knowledge bases for reasoning, planning and rational decision-making in interactions with humans.

The UnityIIS framework is divided into modules to integrate varying agent-modelling and knowledge representation tools. The main modules are 1) the `OWL Unity Package` to enable ontology reasoning, and 2) the `ASP Unity Package` to enable ASP-based action reasoning and planning.

### Prerequisites

Unity Game Engine: https://unity3d.com/get-unity/download

### Installation

* Install Unity
* Create a new Unity 2D/3D project
* Import [UnityIIS](https://github.com/AndreasbCS/Ontology_Unity/blob/a42c57959745da775012adaf584045624af9d38d/UnityIIS.unitypackage)

## Ontology Unity Package
* Integration of an Ontology reasoner in Unity through a web API. 
* The Ontology Unity Package comes with a set of helper functions in C# to do operations with ontologies in Unity.
* This allows Unity-ontology projects to be deployed on any device that has internet access.
* Ontology Unity Package is licensed for academic and research use only (See [license](https://github.com/AndreasbCS/Ontology_Unity/blob/9a950b2f4b3d6eb653e0aaf54441571e8ebd126d/LICENSE)).

### The integrated Ontology reasoner

* Ontology reasoner: BaseVISor
* BaseVISor 2.0.2 is licensed for academic and research use free of charge; all other uses require a commercial license at VIStology, Inc.
* Supported syntaxes: RDF/XML, OWL/XML, All OWL API
* Supported reasoning services: realisation, classification, satisfiability, conjunctive query answering, entailment, consistency.
* Creators of BaseVISor: VIStology, Inc.
* More info: https://www.vistology.com/products/

### Getting started with the Ontology Unity Package

* Copy your .owl file to folder Assets/OntologyModule/encodings/
* In file Assets/OntologyModule/encodings/main.bvr, do the following: 
  * Make sure that relativePath="ontology.owl" is your ontology name. 
* In file Assets/OntologyModule/OntologyWebservice.cs, do the following:
  * Change 'project_key' to your project key, or use the key 'test'
  * Change 'ontology_file_name' to your owl file name, or rename your owl file to 'ontology.owl'

### Start your project

* In file Assets/OntologyModule/encodings/main.bvr, do the following: 
  * Take a look at how example rules are defined to print the results of the OWL inferencing
  * Define the rules you need for your ontology
* In Unity, create a new GameObject
* In Unity, add the script Assets/OntologyModule/OntologyWebservice.cs to a GameObject
* Run the game and check the output from the reasoner in the Unity Console

### Using and adapting the code

* In the script Assets/OntologyModule/OntologyWebservice.cs
  * Parse the text response from the ontology reasoner
  * Define an approrpiate data structure for the response
  * Do application specific operations
    * Function: public void UpdateBVRFile(string input)
      * The function makes procedural changes to main.bvr, such as adding new rules at runtime
      * Any procedural changes are put in the <!-- dynamic content start --><!-- dynamic content end --> section at the end of main.bvr
      * The input string is in RFD format (see example rules in main.bvr)
    * Function: public void UpdateOntologyFile(string input)
      * The function makes procedural changes to ontology.owl, such as adding new facts at runtime
      * Any procedural changes are put in the <!-- dynamic content start --><!-- dynamic content end --> section at the end of ontology.owl
      * The input string is in RFD format (see example facts in ontology.owl)

## Answer Set Programming Unity Package

The ASP Unity Package integrates an Answer Set Programming (ASP) solver and grounder, Clingo, to the Unity platform through a Web API. 
ASP defines a problem in terms of a logic program to enable its logical models (answer sets) to represent the solutions of the original problem. ASP is a declarative programming language to solve difficult, typically NP-hard, search problems, and is particularly useful in for non-monotonic reasoning, knowledge representation, planning, and different action reasoning formalisms. 

UnityIIS comes with a set of helper functions to do operations (e.g., updating, querying) on ASP programs.

### Cite as
```
Brännström, A. (2021). UnityIIS: Interactive Intelligent Systems in Unity (Version 1.0) [Computer software]. https://git.io/JMpzr
```
```
@software{Brannstrom_UnityIIS_2021,
author = {Brännström, Andreas},
month = {12},
title = {{UnityIIS: Interactive Intelligent Systems in Unity}},
url = {https://git.io/JMpzr},
version = {1.0},
year = {2021}
}
```

### Author

* Andreas Brännström {andreasb@cs.umu.se} [Homepage](https://people.cs.umu.se/andreasb/)
* Juan Carlos Nieves<sup>1</sup> {jcnieves@cs.umu.se} [Homepage](https://www.umu.se/en/staff/juan-carlos-nieves/)

Department of Computing Science  
Umeå university  
SE-901 87, Umeå, Sweden  
