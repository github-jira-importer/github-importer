jira-importer.github.com
========================

This repository contains the website that is visible at jira-importer.github.com. It is responsible for the GitHub OAuth redirect of the JIRA GitHub Issue Importer Plugin.

OAuth for GitHub had to be implemented in a special way. During OAuth the application sends a redirect_url to GitHub which should bring
the client back to the local JIRA instance. However, GitHub enforces that this URL matches a pre-configured domain.
Since the host is different for every JIRA instance this does not work for us. We work around this issue by first redirecting the user
to this website which is at a fixed location and then redirect from there to the actual JIRA instance.
