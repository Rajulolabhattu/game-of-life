node('raju'){
    stage('scm'){
        git 'https://github.com/Rajulolabhattu/game-of-life.git'
    }
    stage('build'){
        sh label: 'ubuntu', script: 'mvn package'
    }
    stage('postbuild'){
        archiveArtifacts 'gameoflife-web/target/*.war'
        junit 'jenkins/workspace/gol-02/gameoflife-web/target/surefire-reports/*.xml'
    }

}
