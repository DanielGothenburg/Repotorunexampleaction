# Repotorunexampleaction
This repo is used to run the example action created within another repo called ello-world-docker-action. The action in that repo is called HelloWorldAll.
Name of action is found in the metadatafile for that action. The metadatafile (found in repo ello-world-docker-action) is called action.yml
This is why the file named main in this repo has a reference to ello-world-docker-action/HelloWorldAll
The reference is made by using keyword "uses" followed by the repo hosting the action and the name of the action.
In file main it does not only reference the repo and action name but also supplies an input which is required for the action. This input variable is called "who-to-greet".
Example
uses: ello-world-docker-action/HelloWorldAll
        with:
          who-to-greet: 'Mona the Octocat'

