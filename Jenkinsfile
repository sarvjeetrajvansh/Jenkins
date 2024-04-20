pipeline{
 agent any
 stages{
  stage("Clean Up"){
    steps{
      deleteDir()
    }
  }
  stage("Git clone"){
    steps{
      sh "git clone https://github.com/jenkins-docs/simple-java-maven-app.git"
    }
  }
  stage("Build"){
    steps{
      dir("simple-java-maven-app"){
        sh "mvn clean install"
      } // equal to cd but persistent
    }
  }
  stage("test"){
    steps{
      dir("simple-java-maven-app"){
       sh "mvn test"
      }
    }
  }
 }

}