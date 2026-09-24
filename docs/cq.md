## Competency Questions

PO can be used for answering several questions related to the atomic components that form a document accoridng to certain patterns.
In the following subsections, some of them are introduced together with their respective SPARQL queries. 

The prefixes that are used in all the SPARQL queries provided below are defined as follows:

        PREFIX po: <http://www.essepuntato.it/2008/12/pattern#>

### CQ1

Which header elements are contained within a headed container?
        
        SELECT ?header WHERE {
                ?section a po:headedContainer ;
                        po:containsAsHeader ?header .
        }

### CQ2

Which block elements are directly contained within a container?

        SELECT ?block WHERE {
                ?section po:contains ?block .
                ?block a po:Block .
        }