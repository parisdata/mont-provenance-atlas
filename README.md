# mont-provenance-atlas
PROVENANCE RESEARCH · WIKIDATA P127 EXTRACT Frederick Mont / Galerie Sanct Lucas
Searchable artwork atlas based on results from the following wikidata query:
#title:Artworks that passed through Frederick Mont or Galerie Sanct Lucas 
SELECT DISTINCT ?collection ?collectionLabel  ?item ?itemLabel ?image WHERE {
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],mul,en". }
  {
    SELECT DISTINCT ?item WHERE {
      {
        ?item p:P127 ?statement0.
        ?statement0 ps:P127 wd:Q33315010.
      }
      UNION
      {
        ?item p:P127 ?statement1.
        ?statement1 ps:P127 wd:Q53678062.
      }
    }
  }
  OPTIONAL { ?item wdt:P195 ?collection. }
  OPTIONAL { ?item wdt:P18 ?image. }
}
