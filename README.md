# Demo Project  
  Create a Jenkins Shared Library


# Technologies Used

   Jenkins
   Groovy 
   Docker
   Git
   Java
   maven


# Project Description
  Create a jenkins shared library to extract common build logic

  1. create separate Git repository for Jenkins Shared library Project
  2. Create functions in the JSL to use in the Jenkins pipeline
  3. Integrate and use the JSL in Jenkins pipeline (globally and for specific project)


# Detailed Description of Project
   Create a new project from the code editor (IntelliJ)
   create 'vars' directory
   create a package in the 'src' directory ( eg. com.example)

   create a new groovy file in the package ( eg. Docker.groovy)
   create groovy files with names of all functions (eg buildJar.groovy) in the vars directory
   create all the functions and logic in the class file (eg Docker.groovy) in the "src" directory

  Create a new remote repository and push the files there

  Function can be called in the Jenkinsfile
  
   
  



