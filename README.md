### Install and configure MAVEN project using GIT Repo in Jenkins
Prerequisites: 
1.	Create an account on https://github.com
2.	Create an account on https://mymavenrepo.com
3.	Install git client on Jenkins server (node)
4.	Install JDK (javac) on Jenkins server (node) and set path in Jenkins console.
    # yum install java-1.8.0-openjdk-devel
5.	Add credentials for GITHUB account on jenkins server as below
    Jenkins -> Credentials -> System -> Add Credentials
6. Set JAVA_HOME in Global Tool Configuration
    Click Add JDK -> Nanme = JAVA & JAVA_HOME = /usr/lib/jvm/java-openjdk
7. Also Jenkins needs to know where your Maven is installed, set this in GTC
    Manage plugins -> GCT -> Maven installation -> Add Maven -> Name = maven_3_5_0, check install from Apache. Apply Save. 
8. Install git client on your jenkins server
	# yum install git
9. Set git path in GCT as well. Click git -> Name = Default & Path to git executable = git (Optional)
   
### Workflow Creation in Jenkins console
1. New item -> Select Maven project 
2. Check GitHub Project, Project URL = https://github.com/rajeevsh990/jenkins-example/
3. Check Git in SCM section. Set repository url = https://github.com/rajeevsh990/jenkins-example.git (clone from git web console). select git credentials.
4. Check Build whenever a SNAPSHOT dependency is built (optional)
5. Check GitHub hook trigger for GITScm polling (optional)
6. Build step: Root POM = pom.xml , Goals = clean deploy
7. Apply Save.
8. Build.
