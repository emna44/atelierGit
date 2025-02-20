pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }

    stages {
        stage('GIT') {
            steps {
                git branch: 'master',
                url: 'https://github.com/emna44/atelierGit.git'
            }
        }

        stage ('Compile Stage') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('MVN SONARQUAR'){
	steps {
		sh 'mvn sonar:sonar -Dsonar.login=admin -Dsonar.password=EmnaBorgi21& -Dmaven.test.skip=true';
	}
}
    }
}
