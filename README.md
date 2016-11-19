# node-deploy-server-php-pusher

### Installation
```sh
composer global require capslock-studio/node-deploy-server-php-pusher dev-master

ln -s $HOME/.composer/vendor/bin/deploy-pusher /usr/local/bin/deploy-pusher
```

### How to use
```sh
DEPLOY_HOST={DEFINE_YOUR_NODE_DEPLOY_SERVER} SECRET={DEFINE_YOUR_SECRET} DIST={REMOTE_SERVER_DEPLOY_PATH} deploy-pusher [PARAMETER_WITH_DOUBLE_DASH]
```

### Windows user
```sh
set DEPLOY_HOST={DEFINE_YOUR_NODE_DEPLOY_SERVER}
set SECRET={DEFINE_YOUR_SECRET}
set DIST={REMOTE_SERVER_DEPLOY_PATH}

.\deploy-pusher [PARAMETER_WITH_DOUBLE_DASH]
```

### Shell Parameters
* `--tag`      - Specify the tag you want to deploy
* `--rollback` - Rollback to the previous version
* `--config`   - Load parameter from JSON file
* `--command`  - Command you will execute after deploy successfully.

### ENV
* `SECRET`      - Secret key to encrypt json payload.
* `DEPLOY_HOST` - Server you want to deploy!
* `IGNORE`      - Folders you want to keep.

### Supported CI platform
* TravisCI
* Jenkins
* CircleCI

### Other CI platform
You have to assign `REPO` and `OWNER` to your environment variable in other CI tool.
