pipeline{
    agent{
        label 'jenkins-slave'
    }
    tools{
        maven 'maven-3.8.8'
    }
    environment{
        APPLICATION_NAME = "Eureka"
        SONAR_URL = "http://104.198.166.109:9000"
        SONAR_TOKEN = credentials('sonar_creds')
    }
    stages{
        
        stage('Build'){
            steps{
            echo "********************Building ${APPLICATION_NAME} Application********************"
            sh "mvn clean package"
        }
        }
        stage('CodeQuality'){
            steps{
                echo "********************Running Code Scans******************************"
                sh """
                mvn clean verify sonar:sonar \
                    -Dsonar.projectKey=eureka \
                    -Dsonar.host.url=${SONAR_URL} \
                    -Dsonar.login=${SONAR_TOKEN}
                """
            }
        }
        
    }
}