node {
    stage('Demo stage') {
        deleteDir()
        checkout scm
        archiveArtifacts artifacts: 'bin/demo-binary', fingerprint: true
        step([$class: 'HttpPostPublisher'])
    }
}