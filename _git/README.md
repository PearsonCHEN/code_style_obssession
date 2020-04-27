# Git

[Tips](https://medium.com/walmartlabs/check-out-these-5-git-tips-before-your-next-commit-c1c7a5ae34d1) for `Commit`. 

#### Git Commit Messages

Categorizing commit message is a good habit. It provide with good navigations for reference. I buy the idea from Karma's [blog](http://karma-runner.github.io/0.10/dev/git-commit-msg.html).

#### Format

```bash
<type>: <subject>

<body>

```

##### Possible Type

- feat (new feature for the user, not a new feature for build script)
- fix (bug fix for the user, not a fix to a build script)
- docs (changes to the documentation)
- style (formatting, missing semi colons, etc; no production code change)
- refactor (refactoring production code, eg. renaming a variable)
- test (adding missing tests, refactoring tests; no production code change)
- chore (updating grunt tasks etc; no production code change)
##### Subject

Summary in few words.

##### Massage Body

- use imperative, present tense: “change” not “changed” nor “changes”
- includes motivation for the change and contrasts with previous behavior

More on [365git](https://365git.tumblr.com/post/3308646748/writing-git-commit-messages), Tim Pope's [blog](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html).