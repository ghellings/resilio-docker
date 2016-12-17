# resilio-docker

Resilio bittorret client.  Sync folders between docker containers.  This can be useful for sync'ing folders inside a service in Docker Cloud by using VOLUMES_FROM.

## Usage

Generate secret
```bash
export SECRET=`docker run resilio/sync --generate-secret 2>/dev/null`
```

Run Sync
```
docker run -d -e SECRET=$SECRET SYNCPATH=/path/you/want/to/sync ghellings/resilio
```

