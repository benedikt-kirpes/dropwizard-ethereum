# MicroService Framework for Ethereum
 
1. Developed during Blockchain Summer School Hackathon 2017 Copenhagen, Denmark
2. A full java based implementation for Ethereum using WEB3J. (https://web3j.io)
3. Hibernate MYSQL

## Preconditions:

1. Oracle Java JDK 1.8 (set JAVA_HOME) 
2. Apache Maven 3 (set MAVEN_HOME or M2_HOME)

## generate java class for solidity contract (.sol to .java)

1. add your solidity file into `src\main\resource\`
2. generate by: `mvn web3j:generate-sources`
3. if build sucess, then go to package `generated.contract`

*source https://github.com/web3j/web3j-maven-plugin

## execute microservice

1. from  `dropwizard-ethereum\src\main\resources\config.yml` have a look at mysql credentials (if needed)
2. `cd dropwizard-ethereum`
3. `mvn clean package -U`
4. `java -jar target/dropwizard-ethereum.jar server src/main/resources/config.yml`
5. Web-UI access - `http://localhost:9000/swagger`
