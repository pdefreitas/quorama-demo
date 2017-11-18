node {
    stage('Demo stage') {
        deleteDir()
        checkout scm
        archiveArtifacts artifacts: 'bin/demo-binary', fingerprint: true
        step([$class: 'com.pdefreitas.jenkins.PipelineHttpPostPublisher', url: 'http://51.15.217.142:5000/artifacts/new'])
    }
}