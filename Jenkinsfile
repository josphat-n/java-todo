pipeline { 
  agent any
  tools { 
    gradle "Gradle-8.7"
  }
  stages { 
    stage('clone repository') {
      steps { 
        git 'https://github.com/josphat-n/java-todo'
      }
    }
    stage('Build Project'){
        steps{
            sh 'gradle build'
        }
    }
    stage('Tests') {
      steps { 
        sh 'gradle test'
      }
    }
  }
}