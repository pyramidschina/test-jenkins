node {

    stage('Configure') {
        env.PATH = "/usr/local/apache-maven/bin:${env.PATH}"
        //version = '1.0.' + env.BUILD_NUMBER
        //currentBuild.displayName = version

        //properties([
        //        buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10')),
        //        [$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/bertjan/spring-boot-sample/'],
        //        pipelineTriggers([[$class: 'GitHubPushTrigger']])
        //    ])
    }

    stage('Checkout') {
        git ' https://github.com/pyramidschina/test-jenkins.git'
    }

    stage('Version') {
        //sh "echo \'\ninfo.build.version=\'$version >> src/main/resources/application.properties || true"
        //sh "mvn -B -V -U -e versions:set -DnewVersion=$version"
    }

    stage('Build') {
        sh 'mvn -B -V -U -e clean package'
    }

}