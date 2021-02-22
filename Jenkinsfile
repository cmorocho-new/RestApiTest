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
                sh '/opt/wildfly/bin/jboss-cli.sh --connect --command="deploy --force target/AppTestApi.war"'
            }
        }
    }
}
