pipeline{
  agent any
  tools{
    maven 'MAVEN'
    jdk 'JAVA_HOME'
  }
  stages{
    stage('Code Checkout'){
      steps{
        checkout scm
        bat 'echo code is checked out successfully'
      }
    }
    stage('Build Code'){
      steps{
        mvn clean
        bat 'echo code is build successfully'
      }
    }
    stage('Run Automated Tests'){
      steps{
        mvn test
        bat 'echo automated tests ran successfully'
      }
    }
   
  
  }

}
