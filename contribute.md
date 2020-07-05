# Contributing to p2p-chat

It is warmly welcomed if you have interest to help in p2p-chat. First, we encourage this kind of willing very much. And here is a list of contributing guide for you.

## Topics

- [Contributing to p2p-chat](#contributing-to-p2p-chat)
  - [Topics](#topics)
  - [Reporting security issues](#reporting-security-issues)
  - [Reporting general issues](#reporting-general-issues)
  - [Code and doc contribution](#code-and-doc-contribution)
    - [Workspace Preparation](#workspace-preparation)

## Reporting security issues

Security issues are always treated seriously. As our usual principle, we discourage anyone to spread security issues. If you find a security issue of p2p-chat, please do not discuss it in public and even do not open a public issue. Instead we encourage you to send us a private email to [hizhaxzhax@gmail.com](mailto:hizhaxzhax@gmail.com) to report this.

## Reporting general issues

To be honest, we regard every user of Dragonfly as a very kind contributor. After experiencing Dragonfly, you may have some feedback for the project. Then feel free to open an issue via [NEW ISSUE](https://github.com/Orphans-Paradise/p2p-chat-specification/issues/new).

Since we collaborate project p2p-chat in a distributed way, we appreciate **WELL-WRITTEN**, **DETAILED**, **EXPLICIT** issue reports. To make the communication more efficient, we wish everyone could search if your issue is an existing one in the searching list. If you find it existing, please add your details in comments under the existing issue instead of opening a brand new one.


There are lot of cases when you could open an issue:

* bug report
* feature request
* performance issues
* feature proposal
* feature design
* help wanted
* doc incomplete
* test improvement
* any questions on project
* and so on

Also we must remind that when filing a new issue, please remember to remove the sensitive data from your post. Sensitive data could be password, secret key, network locations, private business data and so on.

## Code and doc contribution

Every action to make project p2p-chat better is encouraged. On GitHub, every improvement for p2p-chat could be via a PR (short for pull request).

* If you find a typo, try to fix it!
* If you find a bug, try to fix it!
* If you find some redundant codes, try to remove them!
* If you find some test cases missing, try to add them!
* If you could enhance a feature, please **DO NOT** hesitate!
* If you find code implicit, try to add comments to make it clear!
* If you find code ugly, try to refactor that!
* If you can help to improve documents, it could not be better!
* If you find document incorrect, just do it and fix that!
* ...

Actually it is impossible to list them completely. Just remember one princinple:

> WE ARE LOOKING FORWARD TO ANY PR FROM YOU.

Since you are ready to improve Dragonfly with a PR, we suggest you could take a look at the PR rules here.

### Workspace Preparation

To put forward a PR, we assume you have registered a GitHub ID. Then you could finish the preparation in the following steps:

1. **FORK** p2p-chat to your repository. You are supposed to choose one repo below.

+ [p2p-chat](https://github.com/zhaxzhax/p2p-chat)

+ [p2p-net](https://github.com/zhaxzhax/p2p-net)

+ [p2p-chat-android](https://github.com/zhaxzhax/p2p-chat-android)

For example as repo [p2p-chat](https://github.com/zhaxzhax/p2p-chat). To make this work, you just need to click the button Fork in right-left of [zhaxzhax/p2p-chat](https://github.com/zhaxzhax/p2p-chat) main page. Then you will end up with your repository in `https://github.com/<your-username>/p2p-chat`, in which `your-username` is your GitHub username.
1. **CLONE** your own repository to develop locally. Use `git clone https://github.com/<your-username>/p2p-chat.git` to clone repository to your local machine. Then you can create new branches to finish the change you wish to make.

1. **Set Remote** upstream to be `https://github.com/zhaxzhax/p2p-chat.git` using the following two commands:

	```
	git remote add upstream https://github.com/zhaxzhax/p2p-chat.git
	git remote set-url --push upstream no-pushing
	```

	With this remote setting, you can check your git remote configuration like this:

	```
	$ git remote -v
	origin     https://github.com/<your-username>/p2p-chat.git (fetch)
	origin     https://github.com/<your-username>/p2p-chat.git (push)
	upstream   https://github.com/zhaxzhax/p2p-chat.git (fetch)
	upstream   no-pushing (push)
	```

	Adding this, we can easily synchronize local branches with upstream branches.

1. **Create a branch** to add a new feature or fix issues

	Update local working directory:

	```
	cd Dragonfly
	git fetch upstream
	git checkout master
	git rebase upstream/master
	```

	Create a new branch:

	```
	git checkout -b <new-branch>
	```

	Make any change on the `new-branch` then build and test your codes.