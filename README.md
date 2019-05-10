# icharts
Helm charts repo.

### How It Works
According to [docs/chart_repository.md at helm/helm](https://github.com/helm/helm/blob/master/docs/chart_repository.md)

I set up GitHub Pages to point to the docs folder. From there, I can create and publish docs like this:
```
$ helm create mychart
$ helm package mychart
$ mv mychart-0.1.0.tgz docs
$ helm repo index docs --url https://isaron.github.com/icharts
$ git add -i
$ git commit -av
$ git push origin master
```
From there, I can do a `helm repo add icharts https://isaron.github.com/icharts`.