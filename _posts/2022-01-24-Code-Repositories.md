---
layout: post
title: "Heritage Connector Code Repositories"
categories: post
---

The [Heritage Connector](https://www.sciencemuseumgroup.org.uk/project/heritage-connector/) project is composed of multiple components and services split across multiple GitHub repos. Below we give an overview of the project's main code repositories:

* [Pipeline](#pipeline)
* [Deployment](#deployment) 
* [Demos](#demos)
* [NLP](#nlp) 
* [Vectors](#vectors)
* [APIs](#apis)
* [Datasets](#datasets)
* [Thor / Fuseki](#fuseki)

## <a name="pipeline"></a>Heritage Connector Pipeline

Contains the main bootstrap / pipeline used by the Heritage Connector to import data into a graph before performing NPL and Graph analysis on it. Individual repos provide much of the actual functionality and are listed separately below.

[https://github.com/TheScienceMuseum/heritage-connector](https://github.com/TheScienceMuseum/heritage-connector)

A set of tools to:

- load tabular collection data to a knowledge graph
- find links between collection entities and Wikidata
- perform NLP to create more links in the graph (also see hc-nlp)
- explore and analyse a collection graph ways that aren't possible in existing collections systems

## <a name="deployment"></a>Heritage Connector Deployment 

An easy way to deploy all the Heritage Connector API’s and Endpoints, with the exception of the main pipeline, in one step.

[https://github.com/TheScienceMuseum/heritage-connector-deployment](https://github.com/TheScienceMuseum/heritage-connector-deployment)

The following services are included and all configured through environment variables:
fuseki - RDF triplestore

- thor - front end for performing SPARQL queries
- thor-cors-proxy - CORS proxy to enable thor to connect to fuseki
- heritage-connector-vectors - an nearest neighbours on knowledge graph embeddings
- heritage-connector-apis - API endpoints to wrap some common SPARQL queries and the nearest neighbours API. 

## <a name="demos"></a>Heritage Connector Demos 

This repo contains various demos and sketches of demos for Heritage Connector. 

[https://github.com/TheScienceMuseum/heritage-connector-demos
](https://github.com/TheScienceMuseum/heritage-connector-demos
)

- an interactive streamlit app showing NER and entity linking which uses static data for speed (not hosted at the moment)
- a bookmarklet to view connections from an SMG collection, blog or journal page
- a macro visualisation of the whole collection/knowledge graph
- a visualisation of the combined SMG and V&A* collections
- maps (map 1; map 2) of all the places in the knowledge graph


## <a name="nlp"></a>Heritage Connector NLP 
NLP tools for heritage collections

[https://github.com/TheScienceMuseum/heritage-connector-nlp
](https://github.com/TheScienceMuseum/heritage-connector-nlp)

## <a name="vectors"></a>Heritage Connector Vectors
Generates graph and language embeddings for the Heritage Connector project.

[https://github.com/TheScienceMuseum/heritage-connector-vectors
](https://github.com/TheScienceMuseum/heritage-connector-vectors)

## <a name="apis"></a>Heritage Connector APIs
Various API’s for the querying Heritage Connector project
[https://github.com/TheScienceMuseum/heritage-connector-apis
](https://github.com/TheScienceMuseum/heritage-connector-apis)

## <a name="datasets"></a>Heritage Connector Data
Various Public data sets for the Heritage Connector Project.

Further public datasets and outputs can be found on the HC / TANC page on Zenodo 

* [https://github.com/TheScienceMuseum/heritage-connector-data](https://github.com/TheScienceMuseum/heritage-connector-data)
* [https://zenodo.org/record/5752010](https://zenodo.org/record/5752010)

## <a name="fuseki"></a>Heritage Connector Thor / Fuseki
These repos provide a SPARQL server (Fuseki), a SPARQL client (Thor) and a Proxy server (to deal with CORS headers)  as Docker containers. All three component can be installed in-one-go via [this repo](https://github.com/TheScienceMuseum/heritage-connector-deployment) 

* [https://github.com/TheScienceMuseum/fuseki-docker](https://github.com/TheScienceMuseum/fuseki-docker)
* [https://github.com/TheScienceMuseum/thor-docker](https://github.com/TheScienceMuseum/thor-docker)
* [https://github.com/TheScienceMuseum/thor-cors-proxy](https://github.com/TheScienceMuseum/thor-cors-proxy)
