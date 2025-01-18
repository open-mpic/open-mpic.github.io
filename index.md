<img src="/images/open-mpic-logo.png" style="float: right; margin: auto; height: 300px" /> 
# What is MPIC?
Multi Perspective Issuance Corroboration or MPIC is the processes of corroborating information required to issue a digital certificate from multiple network perspectives spread across the Internet.
MPIC helps to mitigate the risk of misissuance posed by equally-specific BGP attacks.
CA/Browser Forum requires performing MPIC for the issuance of publicly-trusted web PKI certificates starting March 15, 2025 and halting issuance based on the result of an MPIC check starting September 15, 2025.

# About the Project
The Open MPIC project develops open-source solutions for CAs looking to deploy MPIC.
To support many different CA operations, the Open MPIC project contains various solutions for different deployment models.
Currently, the project provides:
- An API specification
- A core library that is environment agnostic
- Turnkey deployment solutions for CAs to use

# API Documentation

### Take a look at the latest [API documentation here](/documentation.html).

# Codebases maintained by the project
The Open MPIC project maintains the following code bases:

### API Specification ([https://github.com/open-mpic/open-mpic-specification](https://github.com/open-mpic/open-mpic-specification))

This is the Open API specification for Open MPIC.
Our core library is built to implement this specification and clients can be automatically generated from it.

### Open MPIC Core Python ([https://github.com/open-mpic/open-mpic-core-python](https://github.com/open-mpic/open-mpic-core-python))

This is the library that contains the bulk of the MPIC code written in Python.
However, it is written in a manner that is platform/deployment agnostic.
Essentially, the Open MPIC Core does not have any implementation for how to call remote perspectives or load configuration parameters.
Instead, the core library implements all other Open MPIC functions (e.g., CAA checking, DCV checking, selecting perspectives in a way that is CA/B Forum compliant), but leaves the tasks of loading environment variables and passing information from the primary to the remote perspectives to wrapper code that is contained in deployment libraries.
This model allows Open MPIC Core to be platform agnostic and be used regardless of how data is passed between different remote perspectives.

### AWS Lambda Deployment ([https://github.com/open-mpic/aws-lambda-python](https://github.com/open-mpic/aws-lambda-python))

This is a turnkey lambda deployment of Open MPIC using Open MPIC Core. It wraps Open MPIC Core in lambda functions, puts the lambda functions behind an AWS API Gateway and contains Open Tofu deployment scripts to create the system with a single command.

### REST API Deployment ([https://github.com/open-mpic/open-mpic-containers](https://github.com/open-mpic/open-mpic-containers))

This deployment is based on a REST API wrapper around Open MPIC Core which will uses REST API calls between the remote perspectives.
This repo has several deployment examples including docker compose running on EC2, kubernetes, and local docker compose (for testing purposes only).


# Team

We are a community project and anyone is welcome to contribute via pull requests and issues.
We also have a public Slack workspace which can be joined below.
Many people from the community contribute code through pull requests that are merged in.
The below developers are currently in charge of code reviews/pull request evaluations as well as core development/leadership.

- [Henry Birge-Lee](https://henrybirgelee.com) (@Princeton University): Founder, Lead Developer
- Grace Cimaszewski (@Princeton University): Founder, Lead Developer
- [Dmitry Sharkov](https://www.linkedin.com/in/dmitry-sharkov/) (@Sectigo): Lead Architect

We are also proud to recieve engineering support from Princeton University and Sectigo.

# Project Background

The Open MPIC Project was founded by the [Princeton Inspire Research Group](https://github.com/inspire-group/) (P.I. Prof. [Prateek Mittal](https://www.princeton.edu/~pmittal/)). For more background on the Open MPIC Project, read the [blogpost on the project's founding](https://freedom-to-tinker.com/2024/02/13/announcing-the-open-multi-perspective-issuance-corroboration-project/). For more background on MPIC, read the [MPIC history blogpost](https://freedom-to-tinker.com/2024/07/05/a-brief-history-of-multi-perspective-issuance-corroboration/).

# Get Involved
If you are interested in participating in the engineering of Open MPIC, feel free to join the Slack workspace and our mailing list.

### Slack (openmpic.slack.com)
To join the Slack workspace, put your email in below. An invitation will be sent to that email.

<div id="CommunityInviter"></div>
<script>
  window.CommunityInviterAsyncInit = function () {
    CommunityInviter.init({
      app_url:'open-mpic-team',
      team_id:'openmpic'
   })
  };

  (function(d, s, id){
    var js, fjs = d.getElementsByTagName(s)[0];
    if (d.getElementById(id)) {return;}
    js = d.createElement(s); js.id = id;
    js.src = "https://communityinviter.com/js/communityinviter.js";
    fjs.parentNode.insertBefore(js, fjs);
  }(document, 'script', 'Community_Inviter'));
</script>

### Email List (open-mpic@princeton.edu)
To join the mailing list, visit [https://lists.princeton.edu/cgi-bin/wa?A0=OPEN-MPIC](https://lists.princeton.edu/cgi-bin/wa?A0=OPEN-MPIC) and click "Register Password." Fill out the form. Click the link in the email to finalize the new password. Visit [https://lists.princeton.edu/cgi-bin/wa?SUBED1=OPEN-MPIC](https://lists.princeton.edu/cgi-bin/wa?SUBED1=OPEN-MPIC) . Log in with the previously set up email/password. Fill out the subscription form and subscribe to the list. Answer the list subscription confirmation email (may be in spam). Visit [https://lists.princeton.edu/cgi-bin/wa?A0=OPEN-MPIC](https://lists.princeton.edu/cgi-bin/wa?A0=OPEN-MPIC) to see the archives. While anyone can sign up for the list, ONLY REGISTERED USERS THAT ARE SUBSCRIBED TO THE LIST CAN VIEW THE ARCHIVES.