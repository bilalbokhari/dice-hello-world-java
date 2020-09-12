pipeline{
  agent{
    docker{
      image 'maven:3-alpine'
    }
  }
  stages{
    stage('Build'){
      steps{
        sh 'mvn -B -DskipTests clean package'
      }
    }
    stage('Run'){
      steps{
        sh 'java -jar target/hello-world-1.jar'
      }
    }
  }
}
