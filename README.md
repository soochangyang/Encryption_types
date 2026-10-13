# Symmetric Encryption (Shared)
* Using the save key

  ##1 Check Config Server's Dependencies
  * Starting from Spring Boot 2.4, the spring-cloud-starter-bootstrap dependency must be added because bootstrap.yml is no longer loaded by default on startup.
  ```xml
  <dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-bootstrap</artfactId>
  </dependency>
  ```
  #2 Create bootstrap.yml file
  * Configuring encrypt in the bootstrap.yml file applies symmetric key encryption.
  ```properties
  encrypt:
    key: testsymmetricencriptionverylongpassword12345678901234567890
  ```
# Asymmetric Encryption (RSA Keypair)
* Private and Public Key
* Using Java keytool


## Java Cryptography Extension (JCE)
* Download URL -> https://www.oracle.com/java/technologies/javase-jce-all-downloads.html

---
**Download the files from the URL specified above and place them in the designated installation directories for each operating system listed below.
(Applies only to version prior to JDK 21 / Unnecessary from JDK21 onwards)** 

### Windows
* Oracle JDK
{user.home}\Program Files\Java\jdk-13.0.2\conf\security


### MacOS
* Oracle JDK
{user.home}/Library/Java/JavaVirtualMachines/jdk1.8.0_191.jdk/Contents/Home/jre/lib/security

* Open JDK
{user.home}/Library/Java/JavaVirtualMachines/openjdk-14.0.2/Contents/Home/conf/security
