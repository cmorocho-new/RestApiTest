pipeline {
    agent any
    stages {
        stage('-- build --') {
            steps {
                sh 'mvn clean install'
            }
        }
		stage('-- deploy --') {
            steps {
                sh '$WILDFLY_HOME/bin/jboss-cli.sh --connect --command="deploy --force target/AppTestApi.war"'
            }
        }
    }
}