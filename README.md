# Prometheus Workshop

https://dgoldstein1.github.io/git-debugging-workshop/

This repo is a hands-on tutorial to become troubleshooting and debugging with `git`. It consists of:

1. [Hands On Learning](#hands-on-learning)
	1. [Reverting A Pull Request](#reverting-a-pull-request)
	2. [Finding A Bad Commit](#finding-a-bad-commit)
	3. [Finding Issues Merging Into Master](#finding-issues-merging-into-master)
1. [Authors](#authors)
1. [License](#license)


## Hands On Learning

To get the deepest understanding of `git` and the tools it offers, we need to learn at the command line. Below are a few common situations where we have run outside the usual git flow process and we need to dig into our commit histories. Let's begin!

### Reverting A Pull Request

We've all been here. It's late at night and we have a demo early in the morning. You finally solve that issue that's been driving your team crazy. You push up your branch and create a PR. You message your teammate and she quickly merges in your code just before midnight. Everyone gets a good night's sleep.

Your code haunts you in your dream that night and you realize you've made a fatal flaw in your code. You're able to get to the computer before the demo, but only have an hour and you know you can't fix the bug in that time. You know you want to 'undo' last night's merge, but how?!

You go to the [github-documentation](https://help.github.com/en/articles/reverting-a-pull-request) but you realized that you can't just press the 'undo' button because there have been commits since your merge last night.

Let's start by cloning this example locally:

```sh
git clone TODO
```

The current commits `master`, the default branch, look like this:

![revert-current-commit-graph](images/revert-current-commit-graph.png)

Take a second and think. What do we want our *end result* to look like? Simply removing our bad commit from the tree might look enticing, e.g.:

![revert-bad-commit-graph](images/revert-bad-commit-graph.png)

However, not good git. Instead of covering up bad mistakes, it's important we signal to our team (and future developers on our team) that we identified an issue temporarily solved it by reverting our code. Crucially, `git` functions as a linked graph; *it works best by adding commits rather than making edits between commits.* The ideal git graph after reverting our pull request should look like this:

![revert-ideal-commit-graph](images/revert-ideal-commit-graph.png)


### Finding A Bad Commit

### Finding Issues Merging Into Master


## Authors

* **David Goldstein** - [davidcharlesgoldstein.com](http://www.davidcharlesgoldstein.com/?git-debugging-workshop)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

	