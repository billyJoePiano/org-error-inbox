# Fork of Salesfore Org Error Inbox, with OpenAI Integrations removed

This is a fork of <a href="https://github.com/rsoesemann/org-error-inbox">Org Error Inbox</a>, intended for government and highly-regulated industries, where AI usage may be restricted or disallowed.  All OpenAI integrations have been removed from the original package, but it otherwise maintains its core functionality.

# Salesforce Org Error Inbox

Salesforce Orgs can send out notification emails when unhandled exceptions happen in Apex code or Flow or elsewhere. Admins can [define an email adress for this](https://help.salesforce.com/s/articleView?id=000385876&type=1) in the setup. The Org Error Inbox is a native Salesforce App that provides you with an email address to receive those emails. Error emails are parsed and stored in a Custom Object where you can report on and create sophisticated Support workflows.

**Features:**

- **Custom Metadata** Tokenizer for flexible Email Parsing
- Notify **Slack** Channel when email is received
- **Nice Dashboard** with Insights into your Errors

**Video Demo:**

(Note that any OpenAI features mentioned in the video have been removed from this fork)
[![](http://img.youtube.com/vi/RKnqB8bjwdg/hqdefault.jpg)](https://youtu.be/RKnqB8bjwdg "")

## How does it work?

Salesforce orgs send out unhandled errors to the main admin's email address. If you redirect such email to this apps email service, it will receive and parse them into a Custom Object OrgError__c. 

All this information is stored in a single Custom Object and can be easily used for reporting and sophisticated support workflows.

## How can I use it?

Deploy as source to your Production or Sandbox org using the GitHub Salesforce Deploy Tool.

<a href="https://githubsfdeploy.herokuapp.com?owner=billyJoePiano&amp;repo=org-error-inbox&amp;ref=main">
  <img src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/src/main/webapp/resources/img/deploy.png" alt="Deploy to Salesforce" />
</a>

(Unfortunately, this fork of the package is not yet available in Salesforce's App Exchange)


## How can I contribute and extend it?

The project was built as a flexible unnamespaced SFDX project. The repo contains all the scripts to automatically build dev scratch orgs and sample data to play with.

Feel free to fork the repo and extend it. We would love to get improvements as Pull Request from you. Or create issues when you find a problem but don't want to fix it on your own.

---
> NOTE: This app has a [bigger brother for AppExchange partners](https://github.com/rsoesemann/salesforce-isv-cockpit) that want to collect and proactivly manage app errors in their subscribers' orgs.