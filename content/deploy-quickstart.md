---
title: Deploy quickstart
order: 1
description: Learn how to quickly deploy an app to Galaxy with these step-by-step instructions.
---

Galaxy makes it simple to deploy, scale, and monitor your Meteor app. This quickstart guide will walk new users through deploying your first app. It is the abridged version of the [comprehensive guide](/deploy-guide.html) aimed at developers who have experience deploying apps with remote databases.

<h2 id="get-ready-for-deploy">Get your app ready</h2>

Before you begin, [configure access to your MongoDB database](/mongodb.html) and set up any [environment variables](/environment-variables.html) your app depends on using your app’s settings.json file.

<h2 id="deploy-app">Deploy your app</h2>

<h3 id="deploy-mac">Mac and Linux</h3>

On the command line, within your app's directory, type:
```
DEPLOY_HOSTNAME=galaxy.meteor.com meteor deploy [hostname] --settings path-to-settings.json
```

- `hostname` is the fully qualified domain name where you're planning to host your application (for example, 'www.facebook.com').
- `path-to-settings.json` is the path to your settings file (for example, './settings.json').



<h3 id="deploy-windows">Windows</h3>

If you are using Windows, the commands to deploy are slightly different. You need to set the environment variable first, then run the deployment command second (the syntax is the same as everything you'd put for meteor deploy). The commands will look like this:

```
$ SET DEPLOY_HOSTNAME=galaxy.meteor.com
```
```
$ meteor deploy [hostname] --settings path-to-settings.json
```

<h2 id="configure-app">Configure your app</h2>

Once your app is successfully deployed, head on over to your [Galaxy dashboard](http://galaxy.meteor.com) to configure your app by adding a custom domain name and enabling SSL encryption.

Add a domain in your app’s settings and point your DNS to `galaxy-ingress.meteor.com`.

<img src="images/email-add-domain.png" style="">

[Enable encryption](/encryption.html) to secure sensitive data by generating a free [Let’s Encrypt](https://letsencrypt.org) certificate or uploading your own custom certificate.

<img src="images/email-enable-ssl.png" style="width: 300px;">

**Learn more**

- Read our [comprehensive guide](/deploy-guide.html) for deploying apps
- Learn how to [deploy to a specific account](/deploy-guide.html#account-selection)
- Learn how to [transfer apps](/transfer-apps.html) between accounts