# Managing-Heterogeneous-Data-Challenge

## Champions:	
- Michiel van Wijk, TenneT
- Pablo Vicente Legazpi, BDTA
- Mathias Bonduel, Neanex
## Number of people per team: 
4-5
## Anticipated workload:
approx. 24 hours per person, including the time for preparation of the presentation
## Challenge description:
In large projects, multiple data structures such as OTLs, System Breakdown Structure (SBS), Work Breakdown Structures (WBS) are used for managing asset data during the project lifecycle. Each of these data are heterogeneous, i.e. structured differently and must be interconnected to both the BIM models and both relevant documents and drawings. The models and documents thus interconnected as used for both documentation management during the construction phase and also during the handover phase. 
Usually, the Asset Register (a RDBMS structure) contains pre-loaded meta-data about objects (i.e. Assets) in a project. One such meta-data is the “Linked Object type” which points to the corresponding class in an OTL, which is externally stored. This OTL database contains a comprehensive list of all possible objects an asset can have along with their common attributes. And each of these objects point to a set of document IDs (along with meta-data such as document title). These documents can be permit documents for the city administration. Furthermore, a BIM model which contains elements from the Asset Register is also uploaded to a central CDE. 
If the “Linked Object type” is a queryable attribute, how can the four different data sources (Asset Register, OTL, BIM model, and documents) be linked, such both the asset data and the connected document data are always up-to-date? 
## Challenger research questions:
Main research question: How should such a distributed system which uses heterogeneous backend data structuring, be configured so that it can seamlessly capture and maintain up-to-date information, at all times?

What are the minimum data and provenance requirements that should be in place, for ensuring that the distributed system can function throughout the construction phase, where both the document versions and the BIM model will also be constantly changing?

What happens when the OTL and the Assets in the Asset Register are updated? How can impacts on the connected data be managed? 

How can permit documents be connected to the above?

How can such interlinked data be visualized, so that patterns are not missed during querying? Can you propose some improvements to existing tooling with a proof-of-concept extension?
## Datasets available:  
- OTL (as a turtle file)
- Spreadsheet of Assets in the Asset Register,
- Spreadsheet of Documents (and their meta-data), 
- BIM model (IFC, Navisworks),
- Permit documents (as pdfs)		

## Challenge instructions:
There are no restrictions on the reference material to be used. Original ideas for management of heterogeneous data are also encouraged. 
Managing heterogeneous data: 1) View and assess the different data provided in this challenge and their points of commonality. 2) Think about how these data would be linked in a conventional project where domain experts have knowledge.
visualization: 1) Make a list of available tools/methods for dataset visualization and understanding. 2) Evaluate the performance of these tools/methods to get an understanding of the content. 3) Query the dataset using SPARQL, applying the gathered knowledge. 4) Make recommendations and/or extensions to existing tooling.

## Tools needed:
Viewer for visualizing the OTL such as http://vowl.visualdataweb.org/webvowl-old/webvowl-old.html and open-source SPARQL querying tools for querying the RDF data such as https://madsholten.github.io/sparql-visualizer/
Visualization: the list of data visualization tools curated by Vladimir Alexiev, basic statistical SPARQL queries

## References: 
- Understanding CDEs: https://www.bvbs.de/wp-content/uploads/2019/04/Pr%C3%A4sentation_Hartmann__DIN_SPEC_91391.pdf
- ISO 21597, 
- 19650, 
- DIN SPEC 91391
