# git-test
test pulling across branches

## Findings

the following were committed and pushed to origin

* created a file in `main`
* made a change in `main`
* create a new branch `feature/test-two`
* made a change in `feature/test-two`
* made a change in `main`
* merged from `main` and fixed conflict
* made a new file in `main`
* used `git pull origin main --rebase` in `feature/test-two`
  * had to fix the conflicted file again as it had changed in both branches
  * the new file from `main` was pulled into `feature/test-two`

So using `git pull` from another branch will attempt to move changes from that
branch into the current branch which sucks when it's by accident.
