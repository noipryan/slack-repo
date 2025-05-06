# slack-repo

A DNF/YUM repository for installing Slack on RHEL, CentOS, and Fedora Linux.


### Why should I use this repository?

Slack doesn't offer an official repo to use off of their Linux download page. This makes updating the Slack Linux client a manual process, with zero automatic GPG check on the RPM package you are about to install. Also, the install [instructions](https://packagecloud.io/slacktechnologies/slack/install#bash-rpm) on their packagecloud account will give you a repository for automatic package updates, but it uses an invalid GPG key which is less than helpful.

TL;DR: Having automatic Slack for Linux package updates and verifying the GPG signature on the RPM are possible if you use this repo. Yayy!

### Quick start


#### DNF Install
```
sudo dnf config-manager addrepo --from-repofile='https://raw.githubusercontent.com/noipryan/slack-repo/refs/heads/master/slack.repo'
sudo dnf install slack

```

#### Manual Install

```
git clone git@github.com:jdoss/slack-repo.git
cd slack-repo
sudo cp slack.repo /etc/yum.repos.d/slack.repo
sudo dnf install slack
```

# License

MIT License

Copyright (c) 2019 Joe Doss

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
