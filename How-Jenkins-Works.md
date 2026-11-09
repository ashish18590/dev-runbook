# How a Jenkinsfile works
A Jenkinsfile is a text file which tells Jenkins `what to do` when a job runs.
Think of it as a recipe for Jenkins (similar to bitbake).

# Structure (bigger picture)
Every Jenkinsfile has this skeleton
```
pipeline {

  agent { ... }                // WHERE to run (which machine) 
  parameters { ... }           // USER INPUTS (form fields when clicking "Build with Parameters")  
  environment { ... }          // VARIABLES available to all stages
  options { ... }              // JOB SETTINGS (timeout, build history retention, etc.)
  triggers { ... }             // AUTO-TRIGGERS (cron, upstream job, etc.) 
 
  stages { 
      stage('Step 1') { steps { ... } }   // The actual work   
      stage('Step 2') { steps { ... } }
      stage('Step 3') { steps { ... } }
  }
 
  post {   
      always { ... }           // Runs ALWAYS (pass or fail)  
      success { ... }          // Runs ONLY on success
      failure { ... }          // Runs ONLY on failure
      cleanup { ... }          // Runs LAST, after everything else
  }
}
```
