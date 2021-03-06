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

1. Definition
    1. Property of Object
    1. Distinguishes Object from Others
1. Different between UML and IE
    1. UML
        1. ![pict08](pict/chapt3.1.1.jpg)
    1. IE
        1. Existance Based Identity
            1. Identifier Code is automatically generated upon entry
        1. Value Based Identity
            1. Identity consist of real world attributes make up primary key
                1. PROBLEM... lack of attributes leads to problems


#### 2. Derived Data

1. Data computed by stored data
    1. Age from birth date
    1. Pros
        1. More data
    1. Cons
        1. More complications
        1. More bulk
1. Within UML
    1. **milageMonthlyAmount** is derived from **FreqFlyAccount** divided by **30 days**
    1. ![pict08](pict/chapt3.2.1.jpg)
    1. ![pict08](pict/chapt3.2.2.jpg)



#### 3. Current Versus Historical Data

1. Design Decision
    1. Does historical data matter?
        1. Will having a history of past addresses help in any capacity?
        1. Will it hinder or complicate data?
1. ![pict06](pict/chapt3.3.1.jpg)


#### 4. Association Class

1. UML Implementation
    1. ![pict06](pict/chapt3.4.1.jpg)
    1. ![pict06](pict/chapt3.4.2.jpg)
    1. ![pict06](pict/chapt3.4.3.jpg)
    1. ![pict08](pict/chapt3.4.4.jpg)
    1. ![pict08](pict/chapt3.4.5.jpg)
    1. ![pict08](pict/chapt3.4.6.jpg)
1. IE Implementation
    1. ![pict08](pict/chapt3.4.7.jpg)
        1. Identifying relationship = solid line
        1. Non-identifying relationship = dotted line
    1. ![pict08](pict/chapt3.4.8.jpg)
    1. ![pict08](pict/chapt3.4.9.jpg)
        1. ordinary class has UNIQUE IDENTIFIER
    1. Association Class vs Ordinary Class
        1. Association Class
            1. When you want the latest pairing
                1. BUILT INTO IT'S PRIMARY KEY
        1. Ordinary Class
            1. When you want history pairing
                1. History is DISASSOCIATED from PRIMARY KEY

#### 5. Ordered Association

1. Basic Definition
    1. Association that imposes sequencing on Many Association end
1. IE - no ordered association - but combine sequence and AK
    1. ![pict08](pict/chapt3.5.1.jpg)
    1. Adding a sequence number
        1. ![pict08](pict/chapt3.5.2.jpg)
        1. ![pict08](pict/chapt3.5.3.jpg)
        1. ![pict08](pict/chapt3.5.4.jpg)
    1. Combining `flightId` and `sequenceNumber` to form a unique ID
        1. ![pict08](pict/chapt3.5.5.jpg)
        1. ![pict08](pict/chapt3.5.6.jpg)
        1. ![pict08](pict/chapt3.5.7.jpg)
        1. ![pict08](pict/chapt3.5.8.jpg)


#### 6. Qualified Association -(UML)

1. Basic definition
    1. qualifier is an attribute used to identify individual entry
    1. qualified association is a link where all entrys have a qualifier attribute to distinquish themselves in a many association end
1. Within UML
    1. ![pict08](pict/chapt3.6.1.jpg)
    1. ![pict04](pict/chapt3.6.2.jpg)
    1. WARNING WE A USING A DUPLICATE... TWO LOCATIONS FOR `accountNumber`
        1. ![pict08](pict/chapt3.6.3.jpg)
    1. ![pict04](pict/chapt3.6.4.jpg)



#### 7. Qualified Association -(IE)

1. Adding a Qualifier - Via `Constraint`
    1. ![pict06](pict/chapt3.7.1.jpg)
    1. ![pict06](pict/chapt3.7.2.jpg)
    1. ![pict06](pict/chapt3.7.3.jpg)
    1. ![pict06](pict/chapt3.7.4.jpg)
1. Adding `AccountNumber` and `IssuerID`, you get a unique FreqFlyerAccount


#### 8. Large Taxonomies

1. More subject = Larger taxonomies
    1. Hard to comprehend
    1. Instable
    1. A lot of effort
1. Avoid larger than 20 classes
    1. Shift abstraction and use metadata
        1. ![pict06](pict/chapt3.8.1.jpg)
    1. 


#### 9. Package

1. What do you do with a LARGE MODEL
    1. Large diagram of smaller pieces
    1. Division of lesser diagrams, model is spread amongst smaller diagrams
1. UML
    1. Does option 1
1. IE
    1. Does both
1. Lesser Diagram = package
    1. Package = anything made of elements
        1. elements = classes / associations / generalizations
1. Examples
    1. Since, FreqFlyer Model can fit in one page
        1. ![pict06](pict/chapt3.8.2.jpg)
    1. These is no need... but if you need to... 
        1. ![pict08](pict/chapt3.8.3.jpg)
1. In IE... it's called subject area



#### 10. Abridged UML Metamodel

1. Used to review
    1. ![pict06](pict/chapt3.10.1.jpg)
        1. Only shows attributes relevant for associations or generalizations


#### 11. Abridged IE Metamodel

1. Used to review
    1. ![pict06](pict/chapt3.11.1.jpg)


#### 12. Modeling Pitfalls

1. Do **NOT** create a class for a reference
    1. **USE** reference ends
        1. ![pict06](pict/chapt3.12.1.jpg)
1. Avoid parallel attributes
    1. ![pict06](pict/chapt3.12.2.jpg)
1. Avoid **anonymous** attributes
    1. ![pict06](pict/chapt3.12.3.jpg)
1. Avoid Symmetric Associations
    1. Same multiplicity on both ends
    1. ![pict06](pict/chapt3.12.4.jpg)
    1. ![pict06](pict/chapt3.12.5.jpg)
1. Avoid 20+ classes and large models



#### 13. Practical Tips

1. Pay attention to identity
1. Use of existence-based identity
1. Avoid Derived data
1. Qualifier for many assoiciations
1. Avoid large models [4 deep]
1. Aim for simplicity
1. Model review constantly



#### 14. Assessment Test -  Advanced Modeling

1. ![pict08](pict/chapt3.14.1.jpg)
    a. ![pict08](pict/chapt3.14.1.a.jpg)
    b. ![pict08](pict/chapt3.14.1.b.jpg)
    c. ![pict08](pict/chapt3.14.1.c.jpg)
        1. ![pict06](pict/chapt3.14.1.answer.jpg)
1. ![pict08](pict/chapt3.14.2.jpg)
    1. Checking account = existence based identity
    1. Statement = value based identity
    1. ![pict08](pict/chapt3.14.2.answer.jpg)
1. ![pict08](pict/chapt3.14.3.jpg)
    1. ![pict08](pict/chapt3.14.3.answer.jpg)
    1. depends on data 
        1. merely role = wrap
        1. many movie to many people
        1. single movie to many people
1. ![pict08](pict/chapt3.14.4.jpg)
    1. Cascade of qualifications can occur
1. ![pict08](pict/chapt3.14.5.jpg)
    1. Yes. Generalization is allowed. Never exceeds 4 layers or 20 classes.
    1. 









</details>
<hr />





### UML Data Modeling

<details>
<summary>Expand</summary>

#### 1. Problem Statement

1. First Example
    1. ![pict08](pict/chapt4.1.3.jpg)
    1. ![pict08](pict/chapt4.1.1.jpg)
    1. ![pict08](pict/chapt4.1.2.jpg)


#### 2. Finding Classes

1. Read about Ordering Food --> create order class
    1. ![pict08](pict/chapt4.2.1.jpg)
1. Read about one sandwich shop brand with multiple  locations
    1. ![pict08](pict/chapt4.2.2.jpg)
1. Read about multiple menu
    1. ![pict08](pict/chapt4.2.3.jpg)
1. Read about customers
1. Read about menuItems
1. Read about ListPrice
1. Read about Discount
1. Read about Sandwich with bread, cheese, meat
1. Read about Delivery
1. Read about Address
1. Read about Payment and CreditCard
    1. ![pict08](pict/chapt4.2.4.jpg)




#### 3. Finding Associations - Part 1

1.  Think about relationships one at a time
    1. What is the Relationship Between **Order** and **SandwichShop**  website [think in both directions]
        1. One **SandwichShop** website has Many **Orders**
        1. One **Order** has ONLY One **SandwichShop**
        1. Therefore...
            1. One to Many
                1. ![pict04](pict/chapt4.3.1.jpg)
    1. What is the Relationship Between **SandwichShop**  website and **Location** [think in both directions]
        1. One **SandwichShop** website has Many **Location**s
        1. One **Location** has ONLY One **SandwichShop** website
        1. Therefore...
            1. One to Many
                1. ![pict04](pict/chapt4.3.2.jpg)
    1. PROBLEM!! 
        1. What is wrong with this picture?
            1. ![pict04](pict/chapt4.3.3.jpg)
        1. Solution
            1. Orders are based on location NOT ON WEBSITE
            1. ![pict04](pict/chapt4.3.4.jpg)
        1. Moral of the story
            1. Dependency dictates order
    1. Where does **Menu** fit in with **Order**, **SandwichShop**  website and **Location** 
        1. How to break it down
            1. Where does **Menu** vary the most?
        1. **Menu** varys the most with **Location**
            1. ![pict04](pict/chapt4.3.5.jpg)
            
    1. How Does **MenuItem**, **ListPrice** and **Discount** Relate to One Another?
        1. **ListPrice** varies based on **Discount**
        1. **MenuItem** has one **ListPrice**
        1. **MenuItem** can have many **Discount**
        1. **Discount** can apply to many **MenuItem**
        1. ![pict06](pict/chapt4.3.6.jpg)


#### 4. Finding Associations - Part 2

1.  Think about relationships one at a time
    1. What is the Relationship Between **Order** and **Delivery** [think in both directions]
        1. A **Order** MAY or MAY NOT have a means of **Delivery**
        1. **Delivery** method can have many **Orders**
        1. Therefore...
            1. Optional to Many
                1. ![pict06](pict/chapt4.3.7.jpg)
    1. Where does Address fit in? With **Order**? Or with **Delivery**?
        1. It belongs with **Order**.
        1. Since orders can be picked up... 
            1. **Order** MAY or MAY NOT have **Address**
            1. **Address** can be in MANY **Order**'s
                1. ![pict06](pict/chapt4.3.8.jpg)
    1. Where does **Address** fit with **Customer**?
        1. **Address** can have MANY **Customer**
            1. Friend ordering pizza for you
        1. **Customer** MAY or MAY NOT have an **Address**
            1. ![pict04](pict/chapt4.3.9.jpg)
    1. How does **Payment** and **CreditCard** relate to one another?
        1. **Payment** MUST HAVE ONE **CreditCard**
        1. **CreditCard** can apply to MANY **Payment** 
            1. ![pict06](pict/chapt4.3.10.jpg)
    1. How does **Payment** and **Order** relate to one another?
        1. **Payment** can only apply to ONE **Order**
        1. **Order** MAY or MAY NOT have **Payment**
            1. ![pict06](pict/chapt4.3.11.jpg)
    1. How does **Location** and **Address** relate to one another?
        1. **Location** of Sandwich Shop MAY or MAY NOT have an **Address**
        1. **Address** of Sandwich Shop can only be in ONE **Location** 
            1. ![pict06](pict/chapt4.3.12.jpg)
1. Complete Picture
    1. ![pict06](pict/chapt4.3.13.jpg)
    
    
        


#### 5. Finding Generalizations

1. Two ways of finding generalization
    1. Top-down
        1. Requirements dictate structure
    1. Bottom-Up
        1. Models can dictate structure

1. Top-down
    1. Requirement - online ordering
        1. Foods make up the MenuItem
            1. ![pict04](pict/chapt4.5.1.jpg)


#### 6. Iterating And Refining The Model - Part 1

1. Problem - Order can consist of MANY **MenuItem**'s
    1. Two Approaches
        1. Edit the association obetween **Order** and **MenuItem**
            1. Include **quantity** as an attribute
        1. Create another class... **OrderItem**
            1. WHY... symmetry
                1. **Menu** ... **MenuItem**... 
                **Order**... **OrderItem**
            1. ![pict06](pict/chapt4.6.1.jpg)

1. Problem -- how to transfer cost
    1. `OrderItem` needs to be broadened to incl. delivery, sales tax
        1. THEREFORE a `OrderItem` MAY OR MAY NOT have a `MenuItem`
    1. `OrderItem` needs to include the cost AFTER discount
        1. Need to add an attribute of `orderItemAmount`
    1. ![pict04](pict/chapt4.6.2.jpg)



#### 7. Iterating And Refining The Model - Part 2

1. More abstraction for fooditems to incl sauces, type of drink
    1. broadened to be `ItemIngredient`
        1. to include `topping` and `bread` categories
    1. broaded to incl. `IngredientChoice`
        1. to include `white` and `rye` bread
    1. ![pict06](pict/chapt4.7.1.jpg)
1. Problems... can't add constraints... chicken sandwich can become a meatball sandwich
    1. SOLUTION - will be low level code... need to add notes for developers to restrain `IngredientChoice` based on `MenuItem`



#### 8. Adding Attributes

1. Overall workflow
    1. Problem statement focuses on `class` and `associations`
    1. Modeler will need to think through `attributes` of both `class` and `associations`
1. ![pict08](pict/chapt4.8.1.jpg)


#### 9. Cleaning Up Layout

1. ![pict08](pict/chapt4.9.1.jpg)


#### 11. Simplifying The Model

1. Always consider using metadata via specifying every class/subclass

1. Three tiers of data change
    1. Database is hardest
    1. Application is medium
    1. UI is easiest


#### 12. Evolving A Model - Part 1

1. Always look at other apps for ideas
1. Consider guest / sign-in checkout
    1. consider an account-less customer
    1. Account customers
        1. can store credit-cards and addresses
        


#### 13. Evolving A Model - Part 2

1. Adding ad-hoc and account customer
    1. Account customer gets the `address` `perferredAddress` `creditcards` and `perferredCredit`
        1. ![pict08](pict/chapt4.11.1.jpg)
    


#### 14. Enterprise Architect Techniques - Part 1

1. Creating a Blank Project
    1. ![pict06](pict/chapt4.13.1.jpg)
    1. ![pict06](pict/chapt4.13.2.jpg)
    1. ![pict06](pict/chapt4.13.3.jpg)


#### 15. Enterprise Architect Techniques - Part 2

1. Creating a package
    1. ![pict06](pict/chapt4.15.3.jpg)
1. Implementing classes
    1. ![pict06](pict/chapt4.15.1.jpg)
    1. Right-click to add attributes
        1. ![pict06](pict/chapt4.15.2.jpg)
1. Copying class from another package
    1. Left-click from Project Browser... drag into your workspace


#### 16. Enterprise Architect Techniques - Part 3

1. Specify multiplicity
    1. ![pict06](pict/chapt4.16.1.jpg)



</details>
<hr />



### UML into IE Data Modeling
<details>
<summary>Expand</summary>

#### 1. Creating Subject Areas

1. IE takes more space...
    1. If UML is crowded... expect IE to be split
        1. Split based on `Subject Areas`
1. Two subject Areas
    1. Order
        1. ![pict08](pict/chapt5.1.1.jpg)
    1. OrderItem
        1. ![pict08](pict/chapt5.1.2.jpg)
1. When using subject areas...
    1. Think of how they are connected
        1. ![pict04](pict/chapt5.1.3.jpg)


#### 2. Creating Entity Types

1. Create SubjectAreas
    1. ![pict06](pict/chapt5.2.1.jpg)
1. Create Entities within Order
    1. ![pict06](pict/chapt5.2.2.jpg)
1. Create Entities within OrderItem
    1. ![pict06](pict/chapt5.2.3.jpg)


#### 3. Creating Domains

1. Create `objectIdentifier` that is...
    1. Domain parent of **number**
    1. Logical data type of `Long`
        1. ![pict08](pict/chapt5.3.1.jpg)
    1. ![pict08](pict/chapt5.3.2.jpg)
    1. ![pict08](pict/chapt5.3.3.jpg)
    1. ![pict08](pict/chapt5.3.4.jpg)
    1. ![pict08](pict/chapt5.3.5.jpg)
    1. ![pict08](pict/chapt5.3.6.jpg)
    1. ![pict08](pict/chapt5.3.7.jpg)
    1. ![pict08](pict/chapt5.3.8.jpg)
    1. ![pict08](pict/chapt5.3.9.jpg)
    1. ![pict08](pict/chapt5.3.10.jpg)
    1. ![pict08](pict/chapt5.3.11.jpg)
    1. ![pict08](pict/chapt5.3.12.jpg)
    1. ![pict08](pict/chapt5.3.13.jpg)
    1. ![pict08](pict/chapt5.3.14.jpg)

#### 4. Adding Attributes - Part 1

1. Add attributes to each class, domain for each attribute
    1. ![pict08](pict/chapt5.4.1.jpg)
    1. ![pict08](pict/chapt5.4.2.jpg)
    1. ![pict08](pict/chapt5.4.3.jpg)
1. Work on
    1. Account Number
        1. ![pict08](pict/chapt5.4.4.jpg)
    1. Order
        1. ![pict08](pict/chapt5.4.5.jpg)
    1. Delivery Type
        1. ![pict08](pict/chapt5.4.6.jpg)
    1. Location
        1. ![pict08](pict/chapt5.4.7.jpg)
    1. SandwichShop
        1. ![pict08](pict/chapt5.4.8.jpg)
    1. Address
        1. ![pict08](pict/chapt5.4.9.jpg)
    1. Creditcard
        1. ![pict08](pict/chapt5.4.10.jpg)
    1. Payment
        1. ![pict08](pict/chapt5.4.11.jpg)
    



#### 5. Adding Attributes - Part 2

1. More attributes
    1. ![pict08](pict/chapt5.5.1.jpg)
    1. ![pict08](pict/chapt5.5.2.jpg)
    1. ![pict08](pict/chapt5.5.3.jpg)
    1. ![pict08](pict/chapt5.5.4.jpg)
    1. ![pict08](pict/chapt5.5.5.jpg)
    1. ![pict08](pict/chapt5.5.6.jpg)
    1. ![pict08](pict/chapt5.5.7.jpg)
    1. ![pict08](pict/chapt5.5.8.jpg)


#### 6. Creating Relationship Types - Part 1

1. Non Identifying relationship from `Customer` to `Order`
    1. ![pict08](pict/chapt5.6.1.jpg)
    1. ![pict08](pict/chapt5.6.2.jpg)
1. ![pict08](pict/chapt5.6.3.jpg)
1. ![pict08](pict/chapt5.6.4.jpg)
1. 



#### 7. Creating Relationship Types - Part 2

1. Problem...
    1. Account Customer does NOT have a PK
1. Location NEEDS an Address
    1. ![pict08](pict/chapt5.6.5.jpg)


#### 8. Creating Relationship Types - Part 3

1. 



#### 9. Subtyping

1. ![pict08](pict/chapt5.9.1.jpg)


#### 10. Adding Alternate Keys

1. Right click -> Key Group Properties -> Button 'New' -> new alternate key
    1. Good Idea to pick names
        1. ![pict06](pict/chapt5.10.1.jpg)
    


#### 12. ERwin Techniques - Part 1

1. Blank
    1. Go for Logical
1. Difference between Logical / Physical
    1. Available commands
        1. Logical can reverse engineer
        1. Physical
            1. Target a database
            1. Forward Engineer to generate schema
        



#### 13. ERwin Techniques - Part 2

1. Copy a table
    1. ![pict06](pict/chapt5.13.1.jpg)
1. 



</details>
<hr />




### Model Quality
<details>
<summary>Expand</summary>

#### 1. Model Quality

1. Determine database structure
1. Choice of representation
    1. Define difficulty
1. Choices
    1. Normal Form
        1. Defines consistency
    1. Constraint
        1. Boolean condition that data myst satisfy for database storage
    1. Hillard's graph complexity
        1. Equates data model to a undirected graph
        1. Computes complexity
    1. Hoberman's data quality score



#### 2. Normal Forms

1. Guideline for data consistency amoung tables during updates
    1. Types
        1. First
        1. Second
    1. ![pict08](pict/chapt6.2.1.jpg)
    1. ![pict08](pict/chapt6.2.2.jpg)
1. When Normal Forms doesn't get the job done
    1. ![pict06](pict/chapt6.2.3.jpg)
    1. ![pict06](pict/chapt6.2.4.jpg)
1. Why violate Normal Form
    1. Used to increase database READ performance


1. Going over Normal Form 
    1. Starting with a Sales Record
        1. ![pict08](pict/chapt6.2.5.jpg)

    1. Attaining <ins>**1st Normal Form**</ins>

        1. Qualities
            1. Each cell = 1 Value
            1. All entities in column... same type
            1. Each row... MUST BE UNIQUELY IDENTIFIES
        1. What is wrong with the example above...
            1. ![pict08](pict/chapt6.2.6.jpg)
        1. What it should look like..
            1. ![pict08](pict/chapt6.2.7.jpg)

1. Going over <ins>**2nd Normal Form**</ins>
    1. Starting with...
        1. ![pict08](pict/chapt6.2.7.jpg)
    1. Attaining <ins>**2nd Normal Form**</ins>
        1. Qualities
            1. All entries ARE DEPENDENT on Primary Key
        1. What is wrong with the example above...
            1. ![pict08](pict/chapt6.2.8.jpg)
        1. What should it look like...
            1. ![pict08](pict/chapt6.2.9.jpg)

1. Going over <ins>**3rd Normal Form**</ins>
    1. Starting with...
        1. ![pict08](pict/chapt6.2.9.jpg)
    1. Attaining <ins>**2nd Normal Form**</ins> 
        1. Qualities
            1. All entries can be determined ONLY... BY... PRIMARY ...KEY
        1. What is wrong with the example above
            1. ![pict08](pict/chapt6.2.10.jpg)
        1. What it should look like?
            1. ![pict08](pict/chapt6.2.11.jpg)

1. Going over <ins>**4th Normal Form**</ins>
    1. Starting with...
        1. ![pict08](pict/chapt6.2.11.jpg)
    1. Attaining  <ins>**4th Normal Form**</ins>
        1. Qualities
            1. No MULTI-VALUED dependencies
        1. What is wrong with the example above
            1. ![pict08](pict/chapt6.2.12.jpg)
        1. What it should look like?
            1. ![pict08](pict/chapt6.2.13.jpg)


#### 3. Constraints

1. Restriction for database storage
    1. Implicit
        1. Qualifier
            1. Required ID 
                1. Airline ID + Account Number
        1. Generalization Discriminator
            1. Enum-like behavior
            1. Only defined ID win Generalization structure 
    2. Explicit


#### 4. Hillard Graph Complexity

1. ![pict08](pict/chapt6.3.1.jpg)
1. How to calculate?
    1. Longest Traversal
    1. More choice = complication
1. Metrics
    1. Order = total nodes
    1. Size = total edges
    1. Degree = number of edges in a node
    1. Geodesic distance = minimum number of nodes to traverse
    1. Average degree = average edges per node
    1. Average geodesic distance = average edges to traverse between all node pairs
    1. Maximum geodesic distance = largest number edges to traverse between all node pairs

1. ![pict08](pict/chapt6.3.2.jpg)

#### 5. Hoberman Data Model Scorecard

1. ![pict08](pict/chapt6.4.1.jpg)
1. ![pict08](pict/chapt6.4.2.jpg)




</details>
<hr />







### Types of Data Models
<details>
<summary>Expand</summary>

#### 1. Operational Data Models

1. Routine operations [thousands of queries]
1. Online Transaction Processing
1. Why important
    1. Allows change
1. To construct
    1. Start with UML
        1. focus on classes
    2. Work on IE based on UML


#### 2. Enterprise Data Models

1. ENTIRE Organization
1. Only focus on most important
1. Simplified Conceptual model
    1. Typical UML
1. Important for.
    1. Organizational vision
    1. Data consistency
    1. Allow for Reuseable components
    1. Data warehouses
1. Construction process
    1. Application content
    1. Review with business staff


#### 3. Data Warehouses - Part 1

1. Basic Definition
    1. Database dedicated for Analysis and Reports
    1. Maintain history
    1. Focuses on available data and data that has been queried
1. Associated with..
    1. OLAP - OnLine Analytical Processing
    1. ETL - Extract Transform Load
        1. Scripts that reads databases/streams and stores into warehouse
1. Sample
    1. Sandwich Shop
        1. Order Data Warehouse
            1. ![pict08](pict/chapt7.3..jpg)
        1. Datawarehouse would focus on...
            1. Top customers
            1. Are orders affected by...
                1. day of week
                1. holidays
            1. Locations
                1. What has the most orders
        1. OrderItem Data Warehouse
            1. ![pict08](pict/chapt7.3.1.jpg)
        1. Data Warehouse would focus on...
            1. Ingredients
                1. What are the most requested
                1. Does it vary by month
                1. Does advertising affect sales
                
        



#### 4. Data Warehouses - Part 2

1. Star Schema
    1. Basic Definition
        1. Data modeling paradigm surrounded by multiple dimensions
1. Fact
    1. Basic Definition
        1. Table that measures the performance of a business
1. Fact Grain
    1. Basic Definition
        1. Lowest level of detail for which records may be defined
1. Dimension
    1. Basic Definition
        1. Concept that provides a basis for facts
    1. Example
        1. Phone record
            1. setting effective date
            1. expect phone numbers to change
1. Conformed Dimension
    1. Basic Definition
        1. Concept with consistent meaning that is applicable to ALL FACTS in data warehouse





#### 5. Data Warehouses - Part 3

1. Why important
    1. Business Insight
    1. Historical Trends
    1. Understandable
    1. Efficient to get analysis, segregated from day to day
1. Steps to construct
    1. Start woth data marts
        1. Smaller scope and relegate to a developer/team
        1. Must be able to combine with other marts for form larger warehouse
    1. Bus Architecture
        1. Set of Dimensions in all Facts
        1. Avoid summaries, keep facts with most granualar detail
    1. Ideal Outcome
        1. 10-25 facts [tables]
        1. 5-25 dimensions per fact
        


#### 6. Master Data Models

1. Basic Definition
    1. Data Model that standardizes and cleanses the data for critical concept
1. Example
    1. ![pict08](pict/chapt7.6.1.jpg)
1. Why use it
    1. Data Consistency
    1. Avoid Manually cleaning data
    1. Faster Development / Reports
    1. Ideal for Data Warehouses
1. Steps to construct
    1. Determine focus
    1. Start with basic model
    1. Consider existence dependency
        1. other tables will use entries
        1. enforce standards on other tables
1. Example
    1. ![pict08](pict/chapt7.6.2.jpg)



</details>
<hr />











### Database Design
<details>
<summary>Expand</summary>

#### 1. Schema Adjustments

1. Previously on...
    1. Difference between Logical / Physical
        1. Logical
            1. Generated from conceptual model
        1. Physical
            1. Adding design decisions 

1. Starting with the IE model
    1. Examples
        1. ![pict08](pict/chapt8.1.1.jpg)
    1. Each entity type leads to a SQL table
    1. If you need performance 
        1. Merge tables... but
            1. break norm form
    1. Consider SQL reserved words
        1. Google and check 
        1. Order is a reserved word
            1. So... `CustOrder` will work
        1. Name is a reserved word
            1. So... change all attributes with `name` to `nameOfTableName`

#### 2. Attribute Details - Part 1

1. Specify Attribute Details
    1. Data Type
    1. Domain
        1. remember this is a Model-wide restriction of datatype like varchar(30)
    1. Nullability
        1. remember NULL ALLOWED is default 
        1. Before moving to database MUST FIND attributes need to unique define entry
            1. Example...
                1. Customers MUST HAVE A NAME
                    1. ![pict06](pict/chapt8.2.1.jpg)
                1. Account's Password is needed
                1. Order date is needed
                1. Credit Card Attributes are all needed

#### 3. Attribute Details - Part 2

1. ![pict08](pict/chapt8.3.1.jpg)


#### 4. Attribute Details - Part 3

1. Specify Attribute Details
    1. Default Values
        1. Creating a default value in IE
            1. Ideally, we want the database to generate date time of order
                1. ![pict06](pict/chapt8.4.1.jpg)
                1. ![pict06](pict/chapt8.4.2.jpg)
            1. Ideally, when someone orders something... should default to 1
                1. ![pict06](pict/chapt8.4.3.jpg)
1. Once Attributes are fixed... combine SubjectAreas into a ER Diagram
    1. Open Up ER Diagram
        1. ![pict06](pict/chapt8.4.4.jpg)
    1. Change to Physical view (turns model -> code)
        1. ![pict04](pict/chapt8.4.5.jpg)
    1. Forward Engineer to Generate Schema
        1. ![pict04](pict/chapt8.4.6.jpg)
        1. ![pict06](pict/chapt8.4.7.jpg)
        1. Be sure to include...
            1. Table
            1. Column
            1. View
            1. Default Values [of Columns] can show up in either...
                1. CREATE TABLE statement
                1. ALTER statements
            1. Referential Integrity
                1. Ensure AK's and PK's are generated in CREATE TABLE statement
    1. Click on `Preview`
        1. ![pict08](pict/chapt8.4.8.jpg)
    
    



#### 5. Primary And Alternate Keys

1. Primary Key
    1. Unique combination of attributes used for access of each record
    1. CANNOT be null
    1. Table can have AT MOST one PK
1. Alternate Key
    1. Unique combination of sttributes for a table
    1. NONE can be NULL
    1. Can have MULTIPLE AK's 
1. Building ER DIAGRAM
    1. First Concern -- Running out of Object Identifier
        1. Make sure it is autogenerated.
        1. Integer has a limit
        1. To change... access via Domain so change will be read throughout model
            1.  ![pict08](pict/chapt8.5.1.jpg)
        


#### 6. Indexes

1. Basic Defintion
    1. Data Structure that its data fans out in an inverted tree
1. Example
    1. ![](pict/chapt8.6.1.jpg)
1. Advantages
    1. Faster query
    1. Fast FK and PK joins
1. Disadvantages
    1. Slower writes
    1. Consumers more space
1. Different types of indexes
    1. Unique
        1. Enforces uniqueness
        1. Speeds up queries
    1. Non-Unique
        1. Tune performance
    1. Clustered
        1. Physical ordering of table records
        1. Enables faster JOINs
1. Creating Indexes
    1. Ensure every FK has an index
1. In Schema Generation
    1. Enable Foreign Key Indexes
        1. ![pict06](pict/chapt8.6.2.jpg)
    



#### 7. Referential Integrity - Part 1

1. Basic Definition
    1. Guarantee that foreign key reference to PK exists
1. Referential integrity 
    1. Useful for either `update` or `delete` actions to be cascaded from parent to child
1. Best to run with Existence based identification
    1. `update` actions are NOT needed
1. Artificial identifiers
    1. NEVER updated
    1. `delete` action is REQUIRED
1. Referential Integrity Options
    1. NONE
        1. no `update` or `delete` action
    1. Restrict
        1. forbids the deletion of the parent if child was not chosen to be deleted
    1. Cascade
        1. Delete a parent, child goes too
    1. Set Null
        1. Delete a parent, child goes NULL
    1. Set Default
        1. Sets a default action for child if parent is deleted
            
1. Setting RI for Order Model
    1. Setting
        1. View via Logical
    1. Start with Super/Sub Pair
        1. ![pict06](pict/chapt8.7.1.jpg)
        1. ![](pict/chapt8.7.2.jpg)
    1.  Customer to CustOrder relationship
        1. No Action for Parent Delete
            1. Means
                1. NOT permit the deletion of customer record that has orders
    1. CustOrder to Delivery Type
        1. No Action for Parent Delete
        1. DT is metadata... MUST NOT DELETE
        1. None for rest
            1. ![pict06](pict/chapt8.7.3.jpg)
    1. CustOrder to Location
        1. Same as above
            1. ![pict06](pict/chapt8.7.4.jpg)
    1. CustOrder to Address
        1. Because we do NOT WANT address to be deleted
            1. ![pict06](pict/chapt8.7.3.jpg)
    1. Shop to Location
        1. NO ACTION
            1. ![pict06](pict/chapt8.7.3.jpg)
    1. Payment to CustOder
        1. CASCADE - If CustOrder is deleted... payment must go
            1. ![pict06](pict/chapt8.7.5.jpg)
    1. Payment to CreditCard
        1. NO ACTION -- don't want credit card to be deleted b/c someone didn't like what they ordered
            1. ![pict06](pict/chapt8.7.3.jpg)
    1. AccountNumber to PerferredCreditCard
        1. SET NULL
            1. NO ACTION won't work b/c CreditCard can't be deleted just because it is not perferred
        1. ![pict06](pict/chapt8.7.6.jpg)
            1. Same goes for Preferred Address
    1. CreditCard to AccountCust
        1. NO ACTION -- allow customer to change credit details

#### 8. Referential Integrity - Part 2

1. Setting RI for OrderItem Model
    1. OVerall
        1. ![pict08](pict/chapt8.8.1.jpg)
    1. CustOrder and OrderItem
        1. CASCADE -- if we delete an order... must ensure items are deleted
    1. Menu and Location    
        1. NO ACTION -- menu still serves other locations
    1. MenuItem to OrderItem
        1. NO ACTION -- menuitem is metadata
    1. Menu to MenuItem
        1. CASCADE -- Item is part of Menu. When Menu goes... so does its items
    1. OrderItem to Ingredient/Choice
        1. CASCADE
    1. MenuItem to Ingredient
        1. CASCADE - don't want ingredient to be a choice if it was deleted off of menu
1. Including RI in your Schema
    1. ENSURE TO `ALTER TABLE` your Foregin Key
        1. Causes Circular logic if CREATE along with Primary Key
    1. ![pict08](pict/chapt8.8.2.jpg)
        1. Results
            1. ![](pict/chapt8.8.3.jpg)          


#### 9. Check Constraints - Part 1

1.  Correction
    1. Make Preferred Address/CreditCard OPTIONAL
        1. allow for cases of NULL
1. SQL
    1. Allows constrains on
        1. Tables
        1. Domains
        1. Attributes
1. First focus on Domains
    1. CreditCard
        1. Limit it to Visa, MasterCard, Discover
            1. ![pict04](pict/chapt8.9.1.jpg)
            1. ![pict06](pict/chapt8.9.2.jpg)
            1. ![pict06](pict/chapt8.9.3.jpg)
            1. Enable constraint
                1. ![pict06](pict/chapt8.9.4.jpg)
    1. Customer
        1. Limit it to AcctCustomer, AdHocCustomer
            1. ![pict06](pict/chapt8.9.5.jpg)
    1. MenuItem
        1. ![pict06](pict/chapt8.9.6.jpg)
    1. MenuItemSize
        1. ![pict06](pict/chapt8.9.7.jpg)
        1. ![](pict/chapt8.9.8.jpg)

#### 10. Check Constraints - Part 2

1. Attribute Constraints
    1. CreditCard Expiration Dates
        1. ![pict06](pict/chapt8.10.1.jpg)
        1. ![pict06](pict/chapt8.10.2.jpg)
    1. PickupDateTime
        1. ![pict06](pict/chapt8.10.3.jpg)
    1. OrderItem 
        1. ![pict06](pict/chapt8.10.4.jpg)
    1. Complicated 
        1. OrderItem's orderItemName ...
            1. MUST BE NULL ... if... MenuItem exists
            1. MUST BE NOT NULL ... if ... MenuItem NOT exists
        1. DONE on the PHYSICAL TABLE
            1. ![pict06](pict/chapt8.10.5.jpg)
            1. ![pict06](pict/chapt8.10.6.jpg)
    1. Table Constraint on Customer
        1. Either phonenumber or email can be null
            1. ![pict06](pict/chapt8.10.7.jpg)
1. Checking output of constraints and table/column validations
    1. Customer 
        1. ![pict06](pict/chapt8.10.8.jpg)
    1. OrderItem
        1. ![pict06](pict/chapt8.10.9.jpg)        


#### 11. Views

1. Why use Views
    1. Security
        1. Prevent showing complete CreditCard info
    1. Convenience
        1. Generate minutes beform pickup time
1. One constraint
    1. MUST BE IN PHYSICAL
1. Two Views
    1. Create View Table
        1. ![pict06](pict/chapt8.11.1.jpg)
    1. Drag Attributes into View
        1. ![pict06](pict/chapt8.11.2.jpg)
        1. ![pict06](pict/chapt8.11.3.jpg)
        1. ![pict06](pict/chapt8.11.4.jpg)
    1. Take Time to Ensure SQL will properly generate a View
        1. ![pict06](pict/chapt8.11.5.jpg)
            1. PROBLEM -- `adhocCustomerID` is derived from `CustomerID`, which is missing
            1. PROBLEM - `customerType` is NEVER specified
        1. SOLUTION
            1. Within where
                1. ![pict06](pict/chapt8.11.6.jpg)
    1. Do the same for Account
        1. ![pict06](pict/chapt8.11.7.jpg)
1. Check generated schema
    1. ![pict06](pict/chapt8.11.8.jpg)
    1. ![pict06](pict/chapt8.11.9.jpg)


#### 12. Other Aspects Of Design

1. Drop Scripts 
    1. Scripts to drop tables.
    1. Big Problem - maintaining Referential Integrity
        1. Two Approaches
            1. Drop RI then tables
            1. Drop dependent tables first
1. Changing Schema for populated database
    1. MUST MANUALLY WRITE
1. Allocating Storage
1. Access Control
    1. Access, Read, Write
    1. Must be done for security
    1. Best approach
        1. Permissions to Groups
        1. Users to Groups
        
1. Triggers
    1. Don't use too many
        1. can cascade
    1. Ideal for triggering an export to data warehouse
1. Stored Procedures
    1. 




#### 13. Self Assessment Test

1. ![pict06](pict/chapt8.12.1.jpg)
    1. YES
1. ![pict06](pict/chapt8.12.2.jpg)
    1. ALL TRUE
1. ![pict06](pict/chapt8.12.3.jpg)
    1. ALL but A
1. ![pict06](pict/chapt8.12.4.jpg)
    1. First option
1. ![](pict/chapt8.12.5.jpg)
    1. NO, generated SQL schema will have an implicit index.
        1. creating index on AK PK will cause duplicate
1. 



</details>
<hr />












### Creating SQL Server Database
<details>
<summary>Expand</summary>

#### 1. Creating A New Database

1. Easiest way
    1. SQL Server Management Studio
        1. ![pict06](pict/chapt9.1.1.jpg)

#### 2. Executing Schema

1. ![pict06](pict/chapt9.1.2.jpg)
    1. SELECT AND EXECUTE
        1. ![pict06](pict/chapt9.1.3.jpg)



#### 3. Inspecting Metadata

1. 


#### 4. Loading Sample Data

1. 



#### 5. Querying Sample Data

1. 




</details>
<hr />








### Data Modeling Process
<details>
<summary>Expand</summary>

#### 1. Overview

1. Tree
    1. ![pict06](pict/chapt10.1.1.jpg)
1. Opposites
    1. No cycles like..
        1. ![pict04](pict/chapt10.1.4.jpg)        


#### 2. Tree - Hardcoded

1. Basic Defintion
    1. Class at each level
    1. Each level belongs to one parent
        1. ![pict06](pict/chapt10.1.2.jpg)

1. Useful for starting models, not applications



#### 3. Tree - Simple

1. All nodes are the same
    1. differs only in definition
![](pict/chapt10.1.3.jpg)1. 


#### 4. Tree - Structured

1. All nodes
    1. have text/geometric/group
        1. ![pict06](pict/chapt10.1.5.jpg)
    1. Allows nesting and cycles



#### 5. Tree - Overlapping

1. Nodes
    1. can for their own trees
        1. ![pict08](pict/chapt10.1.6.jpg)
    1. need to declare root
    1. nodes are treated uniformally
    1. no cycles

#### 6. Tree - Changing Over Time

1. Model of a management hierarchy where structure NOT change
    1. ![pict06](pict/chapt10.1.7.jpg)
1. Model of a management hierarchy where past, present, future
    1. ![pict08](pict/chapt10.1.8.jpg)
        1. separates person from position
1. Use when things change over time


</details>
<hr />









