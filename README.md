## Charts Repo

This is an charts repository for min-flask helm release.

### How It Works

I set up GitHub Pages to point to the docs folder. From there, I can create and publish docs like this:

```shell
$ # cd your project folder
$ helm package mychart # package helm files to .tgz files
$ helm repo index ./ --url https://wang-kk714.github.io/min-flask-charts/ # generate index.yaml
```

Then, you can upload tgz file and index.yaml to repo.
From there, I can do a `helm repo add <alias> https://wang-kk714.github.io/min-flask-charts/`