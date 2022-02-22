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
    stage('Sonar Analysis'){
      steps{
        withSonarQubeEnv('SonarQube'){
          withMaven(maven:'MAVEN'){
             bat 'mvn clean package sonar:sonar'
          }
        }
      }
    }
  }
  post{
    success{
      bat 'echo pipeline is sucessful'
    }
  }

}
