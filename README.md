## Charts Repo

This is an charts repository for min-flask helm release.

### How It Works

I set up GitHub Pages to point to the docs folder. From there, I can create and publish docs like this:

```shell
$ # cd your project folder
$ helm create mychart # create your helm release files
$ helm package mychart # package helm files to .tgz zip files
$ mv <project-folder>/mychart-0.1.0.tgz chart-repo/docs
$ helm repo index docs --url https://wang-kk714.github.io/chart-repo/ # generate index.yaml
```

From there, I can do a `helm repo add <alias> https://wang-kk714.github.io/chart-repo/`