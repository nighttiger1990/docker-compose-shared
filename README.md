# docker-compose-shared
Share docker-compose file for various engine

```yaml
services:
  client:
    # ...
  db:
    # ...
  npm:
    profiles: ["cli-only"]
    # ...
```
```bash
docker-compose up # start main services, no npm
docker-compose run --rm npm # run npm service
docker-compose --profile cli-only up # start main and all "cli-only" services
```
