node('ubuntu'){
    stage('scm'){
        git 'https://github.com/Rajulolabhattu/game-of-life.git'
    }
    stage('build'){
        sh label: 'ubuntu', script: 'mvn package'
    }
    stage('postbuild'){
        archiveArtifacts 'gameoflife-web/target/*.war'

    }

}