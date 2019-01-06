# Japanese novel template

TODO: Write description.

## Usage

### Setup

    $ git clone https://github.com/fuji-nakahara/japanese-novel-template.git YOUR_NOVEL_TITLE
    $ cd YOUR_NOVEL_TITLE
    $ git remote set-url origin YOUR_REMOTE_REPOSITORY
    $ bundle install && npm install
    $ git grep TODO # and fix them

And enable GitHub Pages and Travis CI.

### Lint

    $ npm run lint

Tweak `.textlintrc` and `prh.yml` for your novel.

### Release ebook

Update the version number in `_config.yml`, commit it and execute:

    $ bundle exec rake tag

### Publish on Kakuyomu and Narou

Create `.deploy-shosetsu.yml`:

```yaml
kakuyomu:
  email: YOUR_KAKUYOMU_EMAIL
  password: YOUR_KAKUYOMU_PASSWORD
narou:
  id: YOUR_NAROU_ID
  password: YOUR_NAROU_PASSWORD
```

And execute:

    $ bundle exec jekyll deploy-kakuyomu --config .deploy-shosetsu.yml,_config.yml --future
    $ bundle exec jekyll deploy-narou --config .deploy-shosetsu.yml,_config.yml --future

## ライセンス

TODO
