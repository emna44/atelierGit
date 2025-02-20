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
                sh 'mvn sonar:sonar -Dsonar.login=squ_d18d01804e6c9683c7fe84db28b26c4027a8d6fe -Dmaven.test.skip=true'		}
	}
    }
}
