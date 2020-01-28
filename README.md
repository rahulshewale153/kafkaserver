# kafkaserver
Introduction
    1. what is Apache kafka?
        Apache kafka is a highly scable and distributed platform for creating and proceessing streams/message in real time.

    kafka is adpated pub sub messaging architecture

        Producer -----------> Message Broker(kafka) -------------> consumer

    kafka is designed by LinkedIn and since 2011 it open source

    2. Kafka Component
       Kafka Broker
       kafka Client
       Kafka Connect
       Kafka Streams
       KSQL

    Producer: Producer send data to kafka as message. suppose we want to send whole table records to kafka so we need to send each record as message to kafka and kafka recevied message from producer

    Consumer: Consumer is consume data which is come from kafka but kafka not send data directly to consumre. kafka wait for consumer request and after consumer request kafka send data to consumer.

    
    What is Kafka Clustre?
        Cluster is group of computer and each running one kafka and perform the common activity.
    
    What is kafka topic?
        topic arbitory name which is given to a data set or unique name for the data stream or message. so consumer and producer receive  and sent data by the topic.
    
    What are topic partition?
        Kafka break topic in smaller partition and this partiton store in distributed kafka. its solve storage capacity problem.

    What is partition offset?
        Partition offset is a kafka message number and its start from 0 and increasing by 1 for every message. but its unique for only partition its not global number. 
        ex. suppose you have kafka cluster and each kafka have partition hence every partition message start from 0.
        
        if you want retrive data from kafka so you need three thing
            topic name -> partition name -> offset number

    what is a consumer group?
        its consumer group. consumer group distribute work load to each other and work together to  perform large operation.  

    What is kafka connect?
        kafka connect to read data from cluster and provider consumer (sink  connector job ) or kafka connect get data from producer and write on kafka cluster (source connector job). 

        we can create mutiple worker to kafka connect. multiple worker  distribute job in each other
        
        kafka connnect responsible for distribute work with worker

        Kafka Connect Architecture?
            1) Worker 
            2) Connectore
            3) Task