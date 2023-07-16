pipeline
{
    agent any
    stages
    {
        stage("build-code")
        {
            steps
            {
                sh "mvn install "
                sh "ls -lrt target/"
            }
        }
        stage("Run Unit Tests"){
            steps {
               sh "mvn test"
            }
        }
        stage('Code Analysis') {
            steps { 
                withSonarQubeEnv('SonarQube'){
               sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
    }
}
