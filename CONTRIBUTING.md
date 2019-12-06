# Contributing to the Topology Grapher

By contributing to Funding Circle, you accept and agree to the following terms
and conditions for your present and future contributions submitted to Funding
Circle. Except for the license granted herein to Funding Circle and recipients
of software distributed by Funding Circle, you reserve all right, title, and
interest in and to your contributions. All contributions are subject to the
following DCO + License terms.

[DCO + License][1]

If you discover issues, have ideas for improvements or new features,
please report them to the [issue tracker][2] of the repository or
submit a pull request. Please, try to follow these guidelines when you
do so.

## Issue reporting

* Check that the issue has not already been reported.
* Check that the issue has not already been fixed in the latest code
  (a.k.a. `master`).
* Open an issue with a descriptive title and a clear, concise and precise statement of the problem
* Mention any pertinent information about the "stack" you are using
  (including Kafka broker/client versions)
* Mention the version (or versions) of the Topology Grapher you're trying to use
* Include any relevant code to the issue summary.

When reporting bugs it's a good idea to go through the [Troubleshooting section
of the manual][8].  Adding information like the backtrace and any sample messages
and/or topic configurations used to the bug report makes it easier to track down bugs.
Some steps to reproduce a bug reliably would also make a huge difference.

## Signoff on Commits

```
# signoff an individual commit
git commit -s -m 'Add foo feature'

# signoff all commits by default
git config format.signoff true

# git alias to rebase sequence of commits to include signoff
[alias]
  signoff-rebase = "!EDITOR='sed -i -re s/^pick/e/' sh -c 'git rebase -i $1 && while test -f .git/rebase-merge/interactive; do git commit --amend --signoff --no-edit && git rebase --continue; done' -"
```

## Pull requests

* Read [how to properly contribute to open source projects on Github][3].
* Keep style and feature PRs separate. Feel free to discuss proposals in #topology-grapher[9]
* Make sure that the unit tests are passing (`lein test`).
* Write [good commit messages][4] and sign each commit (`git commit -s -m 'Add foo feature'`).
* Mention related tickets in the commit messages (e.g. `[Fix #N] Add command ...`).
* Update the [changelog][7].
* [Squash related commits together][6].
* Open a [pull request][5] that relates to *only* one subject with a clear title
  and description in grammatically correct, complete sentences.
* [Sign off][10] on all commits, which certifies that you agree to the [DCO + License][1].

[1]: https://github.com/FundingCircle/topology-grapher/tree/master/doc/DCO_+_LICENSE
[2]: https://github.com/FundingCircle/topology-grapher/issues
[3]: http://gun.io/blog/how-to-github-fork-branch-and-pull-request
[4]: http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
[5]: https://help.github.com/articles/using-pull-requests
[6]: http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html
[7]: https://github.com/FundingCircle/topology-grapher/blob/master/CHANGELOG.md
[8]: https://github.com/FundingCircle/topology-grapher/blob/master/doc/trouble-shooting.md
[9]: https://clojurians.slack.com/messages/CEA3C7UG0/
[10]: https://www.kernel.org/doc/html/v4.17/process/submitting-patches.html#sign-your-work-the-developer-s-certificate-of-origin
