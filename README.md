 
# SPARQL Search System Documentation
This SPARQL search system allows users to query a semantic dataset using SPARQL and receive results in a user-friendly format on a web page. The system uses Javascript and HTML, with Bootstrap for styling.

<!-- Show UI -->
![UI]("./ui.png")

### sample SPARQL queries 

### Get the names and birth dates of all the Presidents of the United States:

```SELECT ?name ?birthdate
--
WHERE {
  ?person a <http://dbpedia.org/ontology/President>;
          <http://dbpedia.org/property/name> ?name;
          <http://dbpedia.org/ontology/birthDate> ?birthdate.
}
ORDER BY ?name
```

### Query to retrieve the names of all the countries in the DBpedia ontology:
``` SELECT DISTINCT ?countryName
WHERE {
  ?country a <http://dbpedia.org/ontology/Country> .
  ?country <http://www.w3.org/2000/01/rdf-schema#label> ?countryName .
  FILTER(LANG(?countryName) = 'en')
}
```



## Credits
-This search system was created by Ganesh Team. It uses Bootstrap for styling, JQuery for AJAX requests, and SPARQL.js for SPARQL parsing. 
-The semantic data used in this search system comes from DBpedia.
