Then we need to use the katacoda_cli.

## Configure the Katacoda environement

Open the follow URL:
[https://www.katacoda.com/create](https://www.katacoda.com/create)
Follow the steps in `CREATE FIRST SCENARIO`, in the second step select `Configure WebHook automatically`.

You will recive an URL like this: `https://github.com/yourprofile/katacoda-scenarios`

Open this URL: [https://www.katacoda.com/yourprofile/settings](https://www.katacoda.com/yourprofile/settings)

At this step in the last URL you will have the follow spaces filled in the previous URL.

```
**Private Github Repository** Yes
**Github Scenario Repository** https://github.com/yourusername/katacoda-scenarios
**Github Webhook Secret** xxxxxx
**Github Deploy Key** ssh-rsa xxxxxx
```

## Clone your katacoda workplace & get the katacoda_cli

**1.- Copy & Paste the text below, substituting in your GitHub userName** in the console.**

`git clone git@github.com:userName/katacoda-scenarios.git`

**2.- Run the follow command:**

`git clone git@github.com:katacodacli/katacoda_cli.git`{{execute}}

**3.- Move to the folder katacoda-scenarios**

`cd katacoda-scenarios`{{execute}}

**4.- Create a new scenario**

First we need to make executable the katacoda_cli file with chmod.

`chmod -x ../katacoda_cli/katacoda_cli`{{execute}}

Then lets proceed to create a katacoda scenario.

`../katacoda_cli/katacoda_cli create scenario`{{execute}}

Fill the required intputs:

```
**Friendly URL:** my-first-scenario
**Scenario Title:** My first katacoda Scenario
**Description:** My first katacoda description
**Environment ImageID:** docker
**Scenario Layout:** terminal
```

Use this examples to put as many things in your scenarios: 
[https://github.com/luisgo1411/katacoda-scenarios](https://github.com/luisgo1411/katacoda-scenarios)