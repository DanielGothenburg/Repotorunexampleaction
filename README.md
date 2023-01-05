# Repotorunexampleaction
This repo is used to run the example action created within another repo called ello-world-docker-action. The action in that repo is called HelloWorldAll.
Name of action is found in the metadatafile for that action. The metadatafile (found in repo ello-world-docker-action) is called action.yml

This is why the file named main2 (you could have given it any name) in this repo has a reference to ello-world-docker-action/HelloWorldAll

To run action above, it requires that the file main2 (in this repo) which is referencing the action, is located in the correct workflows folder (in this repo). Otherwise nothing will happen and you will not see anything under menu "Actions" (in this repo).

The correct workflow folder structure is: .github/workflows

So when file main2 was created you used the path .github/workflows/main2


Inside file main2:

To reference the action:

The reference is made by using keyword "uses" followed by the repo hosting the action and the name of the action.

In file main it does not only reference the repo and action name but also supplies an input which is required for the action. This input variable is called "who-to-greet".

Example

uses: ello-world-docker-action/HelloWorldAll
        with:
          who-to-greet: 'Mona the Octocat'

