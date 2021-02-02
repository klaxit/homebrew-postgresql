# Klaxit Postgresql

Tap with fixed minor versions of PostgreSQL from Homebrew.

## How do I install these formulae?

```sh
brew install klaxit/postgresql/postgresql@12.4
```

Or

```sh
brew tap klaxit/postgresql
brew install postgresql@12.4
```

## How to relese a new version?

### Extract selected version

```sh
brew extract --force --version=12.4 postgresql klaxit/postgresql
```

## Create a PR with new version

```sh
git checkout -b postgres-12.4
git add Formula/postgresql@12.4.rb
git commit --message "postgresql: 12.4"
git push --set-upstream origin postgres-12.4
```

Create a PR then when checks are green, label your PR with the `pr-pull` label.

After a couple of minutes you should observe the PR closed, bottles uploaded and commits pushed to the main branch of your repository.

## How was the initial repo created?

```sh
brew tap-new klaxit/postgresql;
cd $(brew --repository klaxit/postgresql)
git remote add origin git@github.com:klaxit/homebrew-postgresql.git
git push --set-upstream origin main
```
