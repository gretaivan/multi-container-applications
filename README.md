### Study Notes
[Docker Compose 101](https://github.com/getfutureproof/fp_guides_wiki/wiki/Docker-Compose-101)

### Demo Repo
**Setup & Run**
- Clone repo & `cd` into folder
- `git submodule init --update`
- `docker-compose up` or `bash _scripts/start-containers.sh`

**To make changes to submodules** *(Please try this on your own version, not these demo repos!)*
- `cd` into a submodule folder
- `git checkout <a-branch>` (use `git branch` as reference)
- make changes, stage, commit as usual
- push with `git push --recurse-submodules=on-demand`

**To pull remote updates to submodules**
- `git pull --recurse-submodules`

**Teardown**
- `docker-compose down --remove-orphans --volumes` or `bash _scripts/stop-containers.sh`

# Exercises
- Create a parent repo for a pair of services you have worked on eg. a client and a server
- Add the service repositories as submodules with `git submodule add <repo>`
- Add a docker-compose.yaml configuration file to combine a previous project's client and api services