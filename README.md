# ghversioner
Webscraping tool to get release versions of the projects.
Library contains utility methods such as get_release_timestamp and calculate_age_in_days

## How to install

```python
pip install ghversioner
```

## How to use

You'll need to instanciate GitHubUtils. Then you can start populating releases list.

```python
from ghversioner import GitHubUtils

ghv = GitHubUtils(url='https://github.com/spring-projects/spring-boot/releases', pages=5)

check_version = 'v2.7.8'

if ghv.contains_release_version(check_version):
  release_date = ghv.get_release_timestamp(check_version)
  version_age_in_days = ghv.calculate_age_in_days(release_date)

```
