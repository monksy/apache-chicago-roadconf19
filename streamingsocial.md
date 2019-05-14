# Streaming and Social Media using Flink at United

Difficult to catch everyone in social networks.

## Goal 

Social media as an issue tracking DB

## Challenges
 
  - Social CRM to handle 
  - Gathering metrics on user 
  - Lost of state in problems


## Abstraction

 - Identification of who is it
 - Classification, prioritization (what aand how important is the issue)
 - State determination (how did it get there)
 - Recommendation, clustering (are there any recommendations on how to handle the issue?)
 - Routing (who is best equipped to handle the issue) 
 - Latency, fault tolerence, HA, elasticity

## Apache Flink

 - Event driven
 - Event log 
 - State ful streaming 
 - Enrichment 
   - Resource (rest)
   - Seperate stream
 
## External resources 

 - AsyncFunction - queue of promises
  - Can limit backpreasure

## Joins 

  - Tumbling window 
  - Sliding window
  - Session window 
  - Interval join
    - Common key and where elements of stream B have event timestamps that lie in a relative time interval to event timestamps of elemetns in stream a.

## State 

### Options

 - Memory (small)
 - File on disk
 - RocksDB

### Types

  - ValueState (single value)
  - ListState - List of generic items
  - Reducing State -  Single value output
  - Aggregating state - single value that does an agregation and adds to value 
  - MapState - Key value state

## Issues

  - Elastisity
  - Active (flink controlled)/Reactive (external based)
  - JIRA: FLIP-6 https://cwiki.apache.org/confluence/pages/viewpage.action?pageId=65147077

# Tips/Tricks

 - coFlatMap https://darrenjw.wordpress.com/tag/coflatmap/

Concern: Data size and prep (not all data needs to be in flight)
  
## Question

 1. How do you rank quality questions and priority questions? Someone trolling vs an urgent request?

