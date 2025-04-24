# Documentation 
## Sonar
In the ansible playbook we also install sonar, this is a code quality tool that
will help you to see the quality of your code, it will run a scan on the code and
show you the results in the sonar dashboard, you can access it using the ip of the vm.

## Selenium
The last part of the workflow is the selenium test, this is a simple test that 
checks if the application is running and if the login works, and creates a todo
item, you can check the logs to see if it worked. It runs in a docker container in
the githubactions runner, so it should work without any problems.

There is a extra step that is currently commented, if you want to run it locally
you can create a venv with the requirements.txt and run it using behave. You should
also uncomment the headless option in the environment.py file. 
If you run it and get a page that warns the page is not secure, un comment the 
proceed method and it should work fine.

If for any reason the workflow fails to get an ip address for selenium to test it
will default to the localhost.