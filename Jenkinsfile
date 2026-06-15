pipeline{
    agent any
    stages{
        stage('Checkout'){
            stepss{ git https://github.com/laxmiambekar1096/Automation_Projects.git
        }
        stage('Build'){
            steps { sh 'mvn clen install' }
        }
        stage('Test'){
            steps{ sh 'mvn test' }
        }
    }
    post{
        always { junit 'target/surefire-reports/*.xml'
    }
}
