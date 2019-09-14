## Fizz Buzz Example in Java 8 using JUnit 5

### Fizz Buzz is a game where
- if the number is divisible by 3, you say Fizz
- if the number is divisible by 5, you say Buzz
- if neither, you say the number

### Install and configure MAVEN project using GIT Repo in Jenkins
Prerequisites: 
1.	Create an account on https://github.com
2.	Create an account on https://mymavenrepo.com
3.	Install git client on Jenkins server (node)
4.	Install JDK (javac) on Jenkins server (node) and set path in Jenkins console.
5.	Add credentials for GITHUB account on jenkins server as below
    Jenkins -> Credentials -> System -> Add Credentials
6. Set JAVA_HOME in Global Tool Configuration
    Click Add JDK -> Nanme = JAVA & JAVA_HOME = /usr/lib/jvm/java-openjdk
7. If required set git path in GCT as well
   Click git -> Name = Default & Path to git executable = git
