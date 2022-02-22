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
        bat 'mvn clean'
        bat 'echo code is build successfully'
      }
    }
    stage('Run Automated Tests'){
      steps{
        bat 'mvn test'
        bat 'echo automated tests ran successfully'
      }
    }
   
  
  }

}
