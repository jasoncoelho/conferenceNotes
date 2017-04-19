# 8:45am Keynote - Augmented Reality by Blair Macintyre

- ARGON 4
  - Framework tha lets you overlap Augmented Reality on top of Images / Live Stream
  - Demo'd a pretty cool example of the audience with google maps location overlaid
  - Has the ability to replace reality (ie the Live Stream) with an alternate reality 
    - Example - Show a stream from Atl, GA instead of Philly
- ISS Traclabs
  - AR could be used on space missions 
    - showed an image of the EVA suit charger with TEXT overlay
- Usage
  - add a special tag to HTML markup
  
>     <ar-scene>

- Links
  - https://twinery.org/
  - http://www.glitchstudios.co/
  - www.argonjs.io
  - https://aframe.io/

# 10:15am Atomist by Jessica Kerr @jessitron

- Atomist is the company that Rod Johnson joined (or maybe founded???)
- Very similar in process to Spring-Boot 
  - Atomist is a slack based work flow that lets you automate the process of creation of projects in source control and manages **state** in a project management system.
  - In this case, atomist lets you issue commands via slack to generate projects in GitHub via templates, and also automates and track builds in TravisCI, and logs states in GitHub Issues 
  - I think there is preliminary support for JIRA, although the speaker did not seem too enthusiastic about it)
- It isn't rigid i.e you don't need to automate whole work-flow right now
- All code generate by Atomist is PR (Pull-Requests) 
  - this is nice 
- All metadata for Atomist is stored in Neo4J which lets you query the entire state of the project and leverages Neo4J's GUI
- Projects automatically get their own channel in Slack, and this channel lists updates
  - (??? Isn't dependence on Slack an issue ???)
- (??? Is Atomist a hosted solution ???)
- Project templates are stored as Typescript (.ts files)
  - templates have ANTLR and Regexp
  - can potentially write stuff that uses AST, but why bother as regexp will work most of the time
- Templates are cool if you want to standardize patterns 
  - For example, if you wan't to ensure certain things don't get missed example 'CORS'
  - or you want the entire org to learn something new
    - since code changes are PRs, devs aren't obligated to accept it
- (??? RUG ???)
- Bottom line - "Half-assed automation is better than none" - Jessica Kerr
- Links
  - www.the-composition.com

# 11:30am Betting on React Native by Ken Wheeler @ken_wheeler

- Works at Formidable
- React has lifecyle methods
- Has its own stylesheet format
- Has ability to hot reload code into the browser (cool when testing webpages AS this preserves state - no need to type that zipcode everytime you want to test something)
- Cons of React Native 
  - native apps will always be faster
- Can write a AsynBridge to output / render to hardware
- (?? REASON ML ??)
- Need for a new kind of Browser 
  - https://expo.io/
- SNACK - lets you write code on your browser that automatically updates on your phone
  - https://snack.expo.io/
- (?? APPR ??)
 - https://github.com/FormidableLabs/appr

# 1:30pm Stream All Things : Patterns of Modern Data Integration by Gwen Shapira @gwenshap

- Data has transitioned from Data Warehouse to Data Lakes to Data Streams
- Engineering titles have shifted from specialized to more generic (ETL/DBA/Admin to just 'engineer')
- Speaker used a Hotel Chain example to explain how Kafka streams would be useful.
  - Kafka Topics = Database Table
- Compatibility : Confluent Schema registry maintains schema in Avro (alternative frameworks coming soon)
  - this helps refuse / filter messages that are not compatible at the producer stage (and not at the consumer level)
  - errors caught at production rather than consumption
- Data can be removed from the message 
  - Example - obfuscating the credit card info
  - Different consumers can get different level of data
- Scalable consumption
  - Add partitioning to scale based on the slowest consumer
- Kafka Connectors are parallel-izable
- Enriching events 
  - Most apps connect to a DB or REST
  - But this is slow..... so add a cache
  - Cache needs/can to be updated via Kafka messages
- KafkaStreams API
  - Example around Search Relevance 
    - joining a stream to a table 
    - joining 2 streams together
- Note on timestamps 
  - They need to be generated at origin or whatever produces the message
- https://github.com/gwenshap/kafka-clickstream-enrich

# 2:45 pm DevSecOps - lessons learnt from inserting security  

- StarBucks



