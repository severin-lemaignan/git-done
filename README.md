I Git This
==========

Ask Git to tell you what you've been busy with!

This small shell script (bash) does the following:

- for every day:
    - iterate over all your git repositories in your `$HOME`
    - count how many commits you did that day (on any branch)
    - (optionally) send the summary to your [IDoneThis](https://idonethis.com) account

Sample output
-------------

```
$ git-done last week

Git activity on the 2016-01-15:
debian-packages:
-- 3 commits in dlib-18.18
src:
-- 7 commits in academia-website
-- 17 commits in gazr

Git activity on the 2016-01-16:
debian-packages:
-- 1 commits in dlib-18.18

Git activity on the 2016-01-17:
None
```

Usage
-----

```sh
$ ./git-done <starting date>
```

The starting date can be anything that GNU `date` can interpret: for instance,
`last week`, `yesterday`, `2016-01-12`,  `a month ago` all work.

If you want to post the summaries to IDoneThis, simply fill in the `api_token`
and `team_name` variables at the top of the script.

*The script does not yet check if you have already posted a summary for the
given days: if you run the script several times, summaries will be posted
several times! PR welcome :-)*
