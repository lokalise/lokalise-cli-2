# Lokalise CLI v2 Docker image

Docs at https://github.com/lokalise/lokalise-cli-2-go

## Examples

### Download files from Lokalise

```
docker run \
    -v /tmp/locale:/opt/dest \
    lokalise/lokalise-cli-2 lokalise2 \
    --token <token> \
    --project-id <project_id:branch> \
    file download \
    --format json \
    --unzip-to /opt/dest
```
		
### Upload a file to Lokalise

```
docker run \
    -v /tmp/en.json:/opt/src/en.json \
    lokalise/lokalise-cli-2 lokalise2 \
    --token <token> \
    --project-id <project_id:branch> \
    file upload \
    --file /opt/src/en.json \
    --lang-iso en
```
