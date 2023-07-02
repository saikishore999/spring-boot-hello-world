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
                sh "mv target/*.jar target/spring-boot-2-hello-world-1.0.2-SNAPSHOT-${BUILD_NUMBER}.jar"
                sh "ls -lrt target/"
                sh "ls-lrt"
            }
        }
    }
}