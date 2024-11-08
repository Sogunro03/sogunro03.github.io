@prefix : <https://sogunro03.github.io/data#> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix schema: <http://schema.org/> .
@prefix dbpedia: <http://dbpedia.org/resource/> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .

# Define Timmy Sogunro with external links and additional context
:TimmySogunro a foaf:Person ;
    foaf:firstName "Timmy" ;
    foaf:lastName "Sogunro" ;
    schema:email "timmysogunro@gmail.com" ;
    foaf:homepage <https://www.linkedin.com/in/oluwatimilehin-sogunro-075a0615a/> ;
    schema:jobTitle "Student" ;
    
    # Linking Occupation to DBpedia for context
    schema:affiliation dbpedia:University ; # Linking to "University" on DBpedia for context on Student role
    
    # Link Timmy's occupation and relevant topics to external concepts
    schema:knowsAbout dbpedia:Computer_Science, 
                      dbpedia:Artificial_Intelligence,  # Added AI as a related topic
                      dbpedia:Data_Science, 
                      dbpedia:Linked_Data ;

    # Link LinkedIn homepage to LinkedIn's main page for additional context
    foaf:homepage <https://www.linkedin.com/in/oluwatimilehin-sogunro-075a0615a/> ;
    dcterms:source <https://www.linkedin.com> .

# Declare "Student" as a class related to the broader academic concept
:Student a schema:Occupation ;
    owl:sameAs dbpedia:Student ;
    schema:description "An individual engaged in learning at a school or university" .
