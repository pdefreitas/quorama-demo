node {
    stage('Demo stage') {
        deleteDir()
        checkout scm
        archiveArtifacts artifacts: 'bin/demo-binary', fingerprint: true
    }
    stage('Deploy to Quorama') {
        step([$class: 'com.pdefreitas.jenkins.PipelineHttpPostPublisher', url: 'http://127.0.0.1:3000/api/plugins/jenkins/artifacts/add', headers: 'quorama-project=quorama-demo&quorama-api-user=demo&quorama-api-secret=demo'])
    }
}