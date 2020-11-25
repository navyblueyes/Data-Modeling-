<style>
img[alt=pict04] {
   width:40%;
}
img[alt=pict06] {
   width:60%;
}
img[alt=pict08] {
   width:80%;
}
</style>


# Data Modeling

## Notes from Infinite Skills Data Modeling Course

<hr />

### Overview

<details>
<summary>Overview</summary>


1. Development Process
    1. Ascertain business requirements (**busreq**)
    1. Apply busreq's to creating data model
    1. Use **data model** to create **database design**
    1. Use **database design** to implement **database**
1. Two notations
    1. UML for Data Modeling
        1. from Enterprise Architect tool
    1. IE for database design
        1. from Erwin tool
1. Two advanced topics
    1. Data Modeling Patterns
    1. Database Reverse Engineering
1. DBMS
    1. Performance
        1. General Purpose Logic
        1. Concurrent access
        1. Data integrity
        1. Crash Recovery
        1. Data security
    1. Protects against
        1. Programming mistakes
        1. Hardware Failure
        1. Networking Failure
1. Relational Database
    1. Data is read from tables
    1. Tables have number of columns
    1. Tables can have infinite rows
    1. Data entries are the intersection between row and column
    1. Tables can create unique data by matching fields and foreign keys with others
1.  Why focus on Data Models
    1. Reduce Cost
    1. Increase Quality of product
    1. Increase Product production
    1. Increase data performance
    
    

</details>












### Data Model Development Process

<details>
<summary>Chapter</summary>

#### 1. Data Model Notations

1. UML
    1. Unified Modeling Language
    1. Ideal for
        1. conceiving **database models**
    1. Example
        1. ![pict08](pict/chapt1.1.1.jpg)
1. IE
    1. Information Engineering
    1. Ideal for
        1. specific details of **database design**
    1. Example
        1. ![pict08](pict/chapt1.1.2.jpg)


#### 2. UML Versus IE - Conceptual, Logical, and Physical

1. Three Models
    1. Conceptual data model
        1. major entity types
        2. relationship types
    1. Logical data model
        1. attribute types
        1. minor entity types
    1. Physical
        1. Database Design
            1. tables
            1. keys
            1. indices
            1. constraints
1. UML is for
    1. Conceptual 
    1. Logical
1. IE is for
    1. Physical
1. UML is used when...
    1. Researching BusReq
    1. Generate content / scope
1. IE is used when ...
    1. Genereate Code


</details>
<hr />




### Basic Data Modeling

<details>
<summary>Expand</summary>

#### 1. Class and Attribute

1. Object
    1. Concept that has **IDENTITY** and **MEANING** within application
    1. ALSO KNOWN AS... Data
        1. Data Entry
1. Class
    1. Grouping of similar objects
    1. ALSO KNOWN AS... MetaData
        1. Data Table

1. Using UML technology
    1. Creating a new Class / Table
        1. ![pict06](pict/chapt2.1.1.jpg)
        1. ![pict06](pict/chapt2.1.2.jpg)
        1. ![pict06](pict/chapt2.1.3.jpg)
    1. Class and Attribute
        1. ![pict08](pict/chapt2.1.5.jpg)
        1. ![pict06](pict/chapt2.1.6.jpg)
        1. ![pict06](pict/chapt2.1.7.jpg)
    1. BOTH IE and UML...
        1. Have value and attribute
    1. Create a IE entity type
        1. ![pict06](pict/chapt2.1.8.jpg)
        1. ![pict06](pict/chapt2.1.9.jpg)
        1. ![pict06](pict/chapt2.1.10.jpg)
        1. ![pict06](pict/chapt2.1.11.jpg)
        1. ![pict06](pict/chapt2.1.12.jpg)

#### 2. Operation

1. Basic Definition
    1. Function that is applied to/by classes
1. Using within UML
    1. ![pict06](pict/chapt2.2.1.jpg)
    1. ![pict06](pict/chapt2.2.2.jpg)
    1. ![pict04](pict/chapt2.2.3.jpg)


#### 3. Domain

1. Basic Definition
    1. Named set of possible values
        1. Also consider `data type`
        1. specification of attribute's type/size in value
1. Using Domains in IE
    1. ![pict06](pict/chapt2.3.1.jpg)
    1. ![pict06](pict/chapt2.3.2.jpg)
1. Applying Domain to Attributes in IE
    1. ![pict04](pict/ledo21504.png)
    1. ![pict06](pict/chapt2.3.4.jpg)

#### 4. Association Name

1. Basic Defintion
    1. Group of links with common structure / meaning
1. Implemented with
    1. Link
        1. a relationship amoung objects
1. Implement Links within UML
    1. ![pict04](pict/chapt2.4.1.jpg)
    1. ![pict04](pict/chapt2.4.2.jpg)
1. UML vs IE
    1. UML Link
        1. IE Relationship
    1. UML Association
        1. IE Relationship Type
1.  Implement Relationships within IE
    1. ![pict06](pict/chapt2.4.3.jpg)
    1. ![pict06](pict/chapt2.4.4.jpg)
    1. ![pict04](pict/chapt2.4.5.jpg)
    1. ![pict06](pict/chapt2.4.6.jpg)



#### 5. IE Entity Type and Relationship Type

1. Different types
    1. Independent entity type
        1. Primary Key <ins>** NOT INCLUDE**</ins> Foreign Keys
    1. Dependent entity type
        1. Primary Key <ins>**INCLUDES**</ins> Foreign Keys
    1. Difference in IE 
        1. ![pict06](pict/chapt2.5.1.jpg)


#### 6. Association Name

1. Naming Links in UML
    1. ![pict06](pict/chapt2.6.1.jpg)
    1. ![pict06](pict/chapt2.6.2.jpg)
    1. ![pict04](pict/chapt2.6.3.jpg)
    
1. Naming Relationships in IE
    1. ![pict06](pict/chapt2.6.4.jpg)
    1. ![pict06](pict/chapt2.6.5.jpg) 
    1. ![pict06](pict/chapt2.6.6.jpg)

#### 7. Association End

1. Basic Definition
    1. Association with a related class
1. Implementing within UML
    1. ![pict04](pict/chapt2.7.1.jpg)
    1. ![pict06](pict/chapt2.7.2.jpg)
    1. ![pict04](pict/chapt2.7.3.jpg)
1. Implementing within IE
    1. ![pict06](pict/chapt2.7.4.jpg)
    1. ![pict06](pict/chapt2.7.5.jpg)
    1. ![pict06](pict/chapt2.7.6.jpg)


#### 8. Multiplicity - UML

1. Number of occurances <ins>of one class</ins>
    1. relating to a single occurence
        1. <ins>of an associated class</ins>
1. Within UML
    1. creating ONE person IN a FreqFlyAccount
        1. ![pict08](pict/chapt2.8.1.jpg)
    1. creating many FreqFlyAccounts PER Persone
        1. ![pict08](pict/chapt2.8.2.jpg)
    1. OVERVIEW
        1. ![pict08](pict/chapt2.8.3.jpg)
    1. MAY or MAY NOT = 0.1
        1. ![pict06](pict/chapt2.8.4.jpg)

#### 9. Multiplicity - IE

1. Within IE
    1. ![pict06](pict/chapt2.9.1.jpg)
    1. ![pict06](pict/chapt2.9.2.jpg)
    1. ![pcit04](pict/chapt2.9.3.jpg)


#### 10. Generalization - UML

1. Basic Defintion
    1. Creating and differentiating different subclasses within a class
        1. can go forever with levels of subclasses
    1. Example
        1. Airline has general grouping of flights classified as "Activity"
            1. where it needs to track milages
        1. HOWEVER... `"Activity"` can be broken to two subcategories - `FlightActity` and `OtherActivity`
            1. FA needs a field of `serviceClass`
            1. OA needs a field of `activityType`
    1. Implementing Example in UML
        1. ![pict08](pict/chapt2.9.4.jpg)
        


#### 11. Generalization - IE

1. Difference of IE
    1. Instead of superclass(UML)
        1. It is called supertype(IE)
    1. Instead of subclass(UML)
        1. It is called subtype(IE)

1. Implementing in IE (Erwin)
    1. ![pict06](pict/chapt2.11.1.jpg)
    1. ![pict06](pict/chapt2.11.2.jpg)
    1. ![pict06](pict/chapt2.11.3.jpg)
    
    


#### 12. Abstract vs. Concrete Superclass

1. Difference
    1. Abract shows <ins>**all**</ins> subclasses
    1. Concrete shows <ins>**some**</ins> subclasses
1. Implementing Abstract within UML
    1. ![pict04](pict/chapt2.12.1.jpg)
    1. ![pict08](pict/chapt2.12.2.jpg)
    1. ![pict04](pict/chapt2.12.3.jpg)

#### 13. Practical Tips

1. Need to clearly know the Scope/Responsibility of the Database / Customer
1. Understand purpose dictates level of ...
    1. polish
    1. completeness
    1. amount of time
1. Be cautious of names
1. Create lexicon
1. Generalization ONLY if subclasses need differentiation


#### 14. Self Assessment

1. ![pict06](pict/chapt2.14.1.jpg)
1. ![pict06](pict/chapt2.14.2.jpg)
1. ![pict06](pict/chapt2.14.3.jpg)
    1. ![pict08](pict/chapt2.14.3.1.jpg)
1. Which one is the better model
    1. ![pict08](pict/chapt2.14.4.jpg)
1. ![pict06](pict/chapt2.14.5.jpg)
    1. ![pict08](pict/chapt2.14.5.1.jpg)


</details>
<hr />


### Advanced Data Modeling

<details>
<summary>Expand</summary>

#### 1. Identity

1. 


#### 2. Derived Data

1. 



#### 3. Current Versus Historical Data

1. 



#### 4. Association Class

1. 


#### 5. Ordered Association

1. 


#### 6. Qualified Association -(UML)

1. 



#### 7. Qualified Association -(IE)

1. 


#### 8. Large Taxonomies

1. 


#### 9. Package

1. 



#### 10. Abridged UML Metamodel

1. 


#### 11. Abridged IE Metamodel

1. 


#### 12. Modeling Pitfalls

1. 


#### 13. Practical Tips

1. 


#### 14. Assessment Test -  Advanced Modeling

1. 









</details>
<hr />





### UML Data Modeling

<details>
<summary>Expand</summary>

#### 1. Problem Statement

1. 


#### 2. Finding Classes

1. 


#### 3. Finding Associations - Part 1

1. 


#### 4. Finding Associations - Part 2

1. 


#### 5. Problem Statement

1. 


#### 6. Finding Generalizations

1. 


#### 7. Iterating And Refining The Model - Part 1

1. 


#### 8. Iterating And Refining The Model - Part 2

1. 


#### 9. Adding Attributes

1. 


#### 10. Cleaning Up Layout

1. 


#### 11. Simplifying The Model

1. 


#### 12. Evolving A Model - Part 1

1. 


#### 13. Evolving A Model - Part 2

1. 


#### 14. Enterprise Architect Techniques - Part 1

1. 


#### 15. Enterprise Architect Techniques - Part 2

1. 


#### 16. Enterprise Architect Techniques - Part 3

1. 



</details>
<hr />



### UML into IE Data Modeling
<details>
<summary>Expand</summary>

#### 1. Creating Subject Areas

1. 


#### 2. Creating Entity Types

1. 


#### 3. Creating Domains

1. 


#### 4. Adding Attributes - Part 1

1. 



#### 5. Adding Attributes - Part 2

1. 


#### 6. Creating Relationship Types - Part 1

1. 



#### 7. Creating Relationship Types - Part 2

1. 


#### 8. Creating Relationship Types - Part 3

1. 



#### 9. Subtyping

1. 


#### 10. Adding Alternate Keys

1. 



#### 11. Cleaning Up The Layout

1. 


#### 12. ERwin Techniques - Part 1

1. 



#### 13. ERwin Techniques - Part 2

1. 



</details>
<hr />




### Model Quality
<details>
<summary>Expand</summary>

#### 1. Model Quality

1. 


#### 2. Normal Forms

1. 


#### 3. Constraints

1. 


#### 4. Hillard Graph Complexity

1. 



#### 5. Hoberman Data Model Scorecard

1. 




</details>
<hr />







### Types of Data Models
<details>
<summary>Expand</summary>

#### 1. Operational Data Models

1. 


#### 2. Enterprise Data Models

1. 


#### 3. Data Warehouses - Part 1

1. 


#### 4. Data Warehouses - Part 2

1. 



#### 5. Data Warehouses - Part 3

1. 


#### 6. Master Data Models

1. 



</details>
<hr />











### Database Design
<details>
<summary>Expand</summary>

#### 1. Schema Adjustments

1. 


#### 2. Attribute Details - Part 1

1. 


#### 3. Attribute Details - Part 2

1. 


#### 4. Attribute Details - Part 3

1. 



#### 5. Primary And Alternate Keys

1. 


#### 6. Indexes

1. 



#### 7. Referential Integrity - Part 1

1. 


#### 8. Referential Integrity - Part 2

1. 



#### 9. Check Constraints - Part 1

1. 


#### 10. Check Constraints - Part 2

1. 



#### 11. Views

1. 


#### 12. Other Aspects Of Design

1. 



#### 13. Self Assessment Test

1. 



</details>
<hr />












### Creating SQL Server Database
<details>
<summary>Expand</summary>

#### 1. Creating A New Database

1. 


#### 2. Executing Schema

1. 



#### 3. Inspecting Metadata

1. 


#### 4. Loading Sample Data

1. 



#### 5. Querying Sample Data

1. 




</details>
<hr />












### Creating MS Access Database
<details>
<summary>Expand</summary>

#### 1. Generating An ERwin Schema

1. 


#### 2. Creating Tables

1. 


#### 3. Creating Indexes

1. 


#### 4. Creating Constraints And Default Values

1. 



#### 5. Defining Foreign Keys

1. 


#### 6. Creating Views

1. 



#### 7. Loading Sample Data

1. 


#### 8. Querying Sample Data

1. 



</details>
<hr />






### Software Engineering
<details>
<summary>Expand</summary>

#### 1. Development Frameworks

1. 


#### 2. Agile Data Modelling

1. 


#### 3. Documenting A Model - Part 1

1. 


#### 4. Documenting A Model - Part 2

1. 



#### 5. Presenting A Model

1. 



</details>
<hr />







### Data Modeling Process
<details>
<summary>Expand</summary>

#### 1. Overview

1. 


#### 2. Tree - Hardcoded

1. 



#### 3. Tree - Simple

1. 


#### 4. Tree - Structured

1. 



#### 5. Tree - Overlapping

1. 


#### 6. Tree - Changing Over Time

1. 



#### 7. Tree - Degenerate Node and Edge


1. 



</details>
<hr />












### Database Reverse Engineering
<details>
<summary>Expand</summary>

#### 1. Motives

1. 


#### 2. Comparison With Forward Engineering

1. 



#### 3. Outputs

1. 


#### 4. Inputs

1. 



#### 5. Process

1. 


#### 6. Principles

1. 



#### 7. Example - Part 1

1. 


#### 8. Example - Part 2

1. 



</details>
<hr />