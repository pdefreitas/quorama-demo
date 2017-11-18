node {
    stage('Demo stage') {
        deleteDir()
        checkout scm
        archiveArtifacts artifacts: 'bin/demo-binary', fingerprint: true
        step([$class: 'com.pdefreitas.jenkins.PipelineHttpPostPublisher', url: 'http://127.0.0.1:5000/artifacts/new'])
    }
}