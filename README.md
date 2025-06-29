This is a HealthCare Devops Project
Tools used :
✓ Git - For version control for tracking changes in the code files
✓ Jenkins - For continuous integration and continuous deployment
✓ Docker - For containerizing applications
✓ Ansible - Configuration management tools
✓ Selenium - For automating tests on the deployed web application
✓ Terraform - For creation of infrastructure.
✓ Kubernetes – for running containerized application in managed cluster.
This project will be about how to test the services and deploy code to dev/stage/prod etc, just
on a click of button.
Business challenge/requirement
As soon as the developer pushes the updated code on the GIT master branch, the Jenkins
pipeline should be triggered and code should be checkout, compiled, tested, packaged and
containerized. A new test-cluster should be provisioned and configured automatically with all
the required software’s and as soon as the cluster is healthy and available, the application must
be deployed to the test-server automatically using Kubernetes.
The deployment should then be tested using a test automation tool, and if the build is
successful, it should be deployed to the prod server/cluster using Kubernetes. All this should
happen automatically and should be triggered from a push to the GitHub master branch.
Kubernetes cluster must contain at least 2 servers and must be monitored continuously using
Prometheus and dashboard must be visualized using Grafana.
