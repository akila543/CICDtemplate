#Description
This component can be used to create jobs in jenkins along with the configuration automatically.
There are many ways to create jobs automatically in jenkins, one of the way is to create using JENKINS_JOB_BUILDER (python framework).

PRE-REQUISITES TO USE THE COMPONENT:
* Docker must be installed in the system.

# HOW TO USE ?

* Clone the git repository and run this docker command (docker-compose up --build)from the root directory.
  Finally jenkins will be up and running in the port 8080.If you want to change the  jenkins credentials, you can edit
  it in the security.groovy file.
* Run "docker ps" command to see the running containers. Run " docker exec -it --user root container_id /bin/bash" to get into the 
  shell of the docker container.
* Perform the following steps to install the jenkins_job_builder package.
  ==> INSTALL apt-get python-pip && pip install jenkins-job-builder.
* RUN "mkdir /etc/jenkins_jobs" and create a file(jenkins_jobs.ini) inside etc/jenkins_jobs directory.You can find the jenkins_jobs.ini file 
  in the repository.
* Now make a directory called jobs and create yaml files inside the directory. If you want to create a job , mention the job configurations in
  the yaml file and save it in the jobs directory. Repository has YAML files for basic CI/CD jobs such as build, test, deploy and code_quality.
* RUN "jenkins_jobs update jobs" command . Jenkins jobs to perform CI/CD for a java application will be created.