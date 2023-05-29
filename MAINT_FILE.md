# Template for Learning Labs

_**Remove the following italicized text for your README.md file:**_

> _This template repository contains templates for standard non-interactive Labs (`template-lab`), interactive Labs (`template-lab-interactive`), and Jupyter Notebook Labs (`template-jupyter`). Templates for **module** config files are [here](https://wwwin-github.cisco.com/DevNet-PubHub/llabmodules/tree/master/_template), and the template for **track** config files are [here](https://wwwin-github.cisco.com/DevNet-PubHub/llabtracks/tree/master/tracks/_template)._
>
> _A Lab repository contains multiple Labs. Please do NOT create a new repository unless cleared by DevRel Docs & Resources. Use an existing [DevNet-PubHub](https://wwwin-github.cisco.com/DevNet-PubHub) repository whenever possible. Copy a template folder into the existing repo and rename it to create a new Lab._
>
> _If you are creating a new repository, provide a meaningful title for the repository contents in the README._
>
> _For more information about creating Learning Labs, refer to the [Learning Labs Authoring Guide](https://testing-developer.cisco.com/pubhub/docs/4662/new/)._

Learning Labs are written in Markdown. A `config.json` organizes the content and defines the order. The `config.json` file also can point to a development environment and default code file if needed. You use PubHub projects at [https://pubhub.cisco.com](https://pubhub.cisco.com) to publish the content.

When you have access to a PubHub project, it shows in the My Projects list. Any Collaborator on a PubHub project can add another Collaborator.

You can write [Markdown](https://www.markdownguide.org/basic-syntax) in a plain text editor, and desktop and Web-based options allow you to simultaneously write and preview your work. We recommend Visual Studio Code [Download](https://code.visualstudio.com/) with one of the [extensions available for Markdown preview](https://code.visualstudio.com/docs/languages/markdown).

You can validate a JSON file by using an [online formatter and validator](https://jsonformatter.curiousconcept.com) or by using [VS Code for JSON editing](https://code.visualstudio.com/Docs/languages/json).

## PubHub projects

_As you create the Learning Labs and Modules, update the following tables in the README._

| Lab ID             | PubHub project        |
|--------------------|-----------------------|
| **LAB ID HERE**    | **PUBHUB URL HERE**   |

## Modules

| Module ID          | PubHub project        |
|--------------------|-----------------------|
| **MODULE ID HERE** | **PUBHUB URL HERE**   |

## Tracks

| Track ID           | PubHub project        |
|--------------------|-----------------------|
| **TRACK ID HERE**  | **PUBHUB URL HERE**   |

## How to run the devenv container to test locally

You can run the development environment (devenv) container locally by running the `Dockerfile` for the devenv. 

This example runs the `devenv-dne` container for testing purposes locally:

```bash
CONTAINER="devenv-dne" IMAGE="developenv/devenv-dne:latest" &&
  docker stop ${CONTAINER} | true &&
  docker rm ${CONTAINER} | true &&
  docker run --platform linux/amd64 --name ${CONTAINER} -d -p 1001:9090 -p 1002:9091 -p 1003:8080 \
    -e "DEVENV_PASSWORD=secret" \
    ${IMAGE} &&
  echo http://localhost:1001?arg=secret 
```

## How to make a Learning Lab interactive

When you want to add a development environment to launch with the **Start Learning** button on the first page, edit the `config.json` file to ensure it has an `id` value for the `devEnv` `config` section. For example:

```json
"config": {
    "devEnv": {
       "id" : "devenv-dne"
              }
          } 
```

Optionally, you can add a default file to open in the editing window when the devenv container launches using the `defaultFile` configuration:

```json
"config": {
    "devEnv": {
      "id": "devenv-base",
      "defaultFile": "src/meraki-code/meraki-mission-2/webhookreceiver.py"
              }
           }
```

While only the `devEnv` setting is required, the environment should open with a default file to enhance the student's experience.

## How to review the integrated learning experience

When you have made the code and content changes and tested the container locally, create a Pull Request to this `llabsource-*` repository.

Review and merge to the default branch.
Go to [https://pubhub.cisco.com](https://pubhub.cisco.com) and click the **Learning Labs** icon in the left-hand pane to see the list of Learning Labs.

Click the one you want to publish and then click **Sync**. A second preview tab appears and you can see the generic rendering of the content.

Next, click **Request to publish** and the system sends a notification to approvers who can publish the Learning Lab. You also receive an email indicating who can publish for you.

Once approved, go to the staging server (testing-developer.cisco.com) to review the entire Learning Lab as intended.

## How to put the Learning Lab into a Track or Module

The **llabtracks** repository at [https://wwwin-github.cisco.com/DevNet-PubHub/llabtracks](https://wwwin-github.cisco.com/DevNet-PubHub/llabtracks) contains the JSON files and links to the PubHub projects that publish Tracks. The **llabmodules** repository at [https://wwwin-github.cisco.com/DevNet-PubHub/llabmodules](https://wwwin-github.cisco.com/DevNet-PubHub/llabmodules) contains the JSON files and links to the PubHub projects that publish Modules.

The JSON files point to the references using the **Lab ID** for each Learning Lab. So when you want a Learning Lab in a Track, you put it in the correct location order in the `config.json` file for that track. A folder corresponds to each track. For DevNet Express, there's a separate folder to collect those Tracks.

## Getting involved

If you're interested in creating a new Cisco DevNet Learning Lab, please contact a DevNet administrator for guidance.
