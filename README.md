#Windows Azure Active Directory SDK for node.js

This Node.js package will give you with a quick and easy way to set up your first app that's integrated with Windows Azure Active Directory. The sample apps included in download are designed to run on any platform. It also provides libraries so you can build your own node.js applications using Passport.js.

Start with either the WS-Federation or SAML-P passport.js strategy, and then access the Windows Azure Active Directory Graph API. By the end of these walkthroughs, you should be able to build a running HTTP server with the following features:

* WebSSO using WS-Federation or SAML-P
* Graph API query capabiltiy using OpenAuth 2.0

[Refer to our Wiki](https://github.com/MSOpenTech/passport-azure-ad/wiki) for detailed walkthroughs on how to use this package.

We've released all of the source code for this running example in GitHub under an Apache 2.0 license, so feel free to clone (or even better, fork!) and provide feedback on the forums.

## Quick Start

Getting started with the sample is easy. It is configured to run out of the box with minimal setup. 

### Step 1: Register a Windows Azure AD Tenant

To use this sample you will need a Windows Azure Active Directory Tenant. If you're not sure what a tenant is or how you would get one, read [What is a Windows Azure AD tenant](http://technet.microsoft.com/library/jj573650.aspx)? or [Sign up for Windows Azure as an organization](http://www.windowsazure.com/en-us/manage/services/identity/organizational-account/). These docs should get you started on your way to using Windows Azure AD.

### Step 2: Generate A Service Principal for your Windows Azure AD Tenant

After you get your Windows Azure AD tenant, add this sample app to your tenant so it can access your tenant information. If you need help with this step, see: [Learn how to register and integrate an application with Windows Azure AD](http://msdn.microsoft.com/en-us/library/windowsazure/dn151122.aspx) and [Adding, Updating, and Removing an App](http://msdn.microsoft.com/en-us/library/windowsazure/dn132599.aspx).

### Step 3: Download node.js for your platform
To successfully use this sample, you need a working installation of Node.js.

Install Node.js from [http://nodejs.org](http://nodejs.org). 

### Step 4: Download the Sample application and modules

Next, clone the sample repo and install the NPM.

From your shell or command line:

* `$ git clone https://github.com/MSOpenTech/AzureAD-Node-Sample`
* `$ npm install`

### Step 5: Add Configuration Values and Run Application

For using the WS-Federation protocol:

* `$ cd login-wsfed`
* `$ node app.js`

For using the SAML-P protocol:

* `$ cd login-saml`
* `$ node app.js`

The login credentials for the sample application are:

Username: `aaUser@graphDir1.onMicrosoft.com`

Password: `P@ssword1`


The configuration values you'll need to edit are found in ```app.js ``` and documented in the code. As much as possible they will match the fields in the Azure Management Portal as discussed in [Adding, Updating, and Removing an App](http://msdn.microsoft.com/en-us/library/windowsazure/dn132599.aspx).

## Detailed Information


###The Technologies In This Demo

The website in this sample app demonstrates the following technologies from the Windows Azure AD from Microsoft, and includes open source modules for each scenario.

- Web Single Sign-In (WebSSO): ``` passport-azure-ad```
- Access to Windows Azure Active Directory through a RESTful Graph API: ```node-waad```


#### Web SSO: [Windows Azure Active Directory Passport.js Plug-In](https://github.com/MSOpenTech/passport-azure-ad)

With Windows Azure AD Web Single Sign-On (WebSSO) you will have the ability to seamlessly integrate your node.js application in to your existing identity platform while using the same credentials you use in the office and online.

For more information on how this module works, refer to the [README](https://github.com/MSOpenTech/passport-azure-ad) in the provided module or read it online.

#### Graph API: [Auth0's Javascript REST library for Windows Azure AD](https://github.com/auth0/node-waad)

Windows Azure AD Graph API lets you build data-driven applications using a REST-based API. You can use this REST API to query your customer data, find relationships in the directory, and customize your apps based on customer data.

For more information on how this module works, see the [README](https://github.com/auth0/node-waad) in the module or read it online.



## About The Code

Code hosted on GitHub under Apache 2.0 license

### Acknowledgements 

We would like to acknowledge the folks who own/contribute to the following projects for their support of Windows Azure Active Directory and their libraries that were used to build this sample. In places where we forked these libraries to add additional functionality, we ensured that the chain of forking remains intact so you can navigate back to the original package. Working with such great partners in the open source community clearly illustrates what open collaboration can accomplish. Thank you!

* Auth0's [WS-Federation and SAML parsing library](https://github.com/auth0/passport-wsfed-saml2)
* Auth0's [Graph API Javascript library](https://github.com/auth0/node-waad)
* Auth0's [SAML-P Library](https://github.com/auth0/node-saml)


[passport-wsfed]: https://github.com/WindowsAzureAD/passport-wsfed-saml2
[node-waad]: https://github.com/WindowsAzureAD/activedirectoryauthenticationlib-sdk-for-node

