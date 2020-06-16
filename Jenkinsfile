pipeline {
    agent { node { label 'rajupk' } }
    stages {
        stage( 'clone and compile' ) {
            steps {
                git branch: 'master',
                url: 'https://github.com/Rajulolabhattu/game-of-life.git'
            }
        }
        stage( 'build' ) {
            steps{
                sh 'mvn clean package'
            }
        }
    }
}
