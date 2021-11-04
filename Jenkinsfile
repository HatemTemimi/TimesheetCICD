node{
     
    stage('cloning') {
    
       git 'https://github.com/HatemTemimi/TimesheetCICD'
    
     }

    stage('Cmpl & Pkg') {

    sh 'mvn -DskipTests=true package'
   
    }

    stage('Artifact Deploy'){
    
    nexusArtifactUploader artifacts: 
                          [[
                          artifactId: 'timesheet',
                          classifier: '', 
                          file: '/var/lib/jenkins/workspace/MyPipe/target/timesheet-1.0.war', 
                          type: 'war'
                          ]], 
                          credentialsId: 'nexus2', 
                          groupId: 'tn.esprit.spring',
                          nexusUrl: 'localhost:8081/nexus/',
                          nexusVersion: 'nexus2', 
                          protocol: 'http', 
                          repository: 'timesheet-snapshots/', 
                          version: '1.0'
    
    }

}
