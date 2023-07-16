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
    }
}
