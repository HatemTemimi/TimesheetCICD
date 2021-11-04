node{
     
    stage('cloning') {
    
       git 'https://github.com/HatemTemimi/TimesheetCICD'
    
     }

    stage('Cmpl & Pkg') {

    sh 'mvn -DskipTests=true package'
   
    }

    stage('Artifact Deploy'){
    
    sh 'mvn -DskipTests=true deploy'
    
    }

}
