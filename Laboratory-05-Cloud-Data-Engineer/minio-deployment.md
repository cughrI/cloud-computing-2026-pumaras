# MinIO Deployment Documentation

## Docker Command Used

> **Note:** The lab's original command uses `minio/minio`, but MinIO discontinued free Docker Hub images in October 2025, so that image is no longer pullable. This deployment uses `tobi312/minio`, a community-maintained image with an identical command-line interface and environment variables, as a drop-in replacement.

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  tobi312/minio:latest server --console-address ":9001" /data
```
<img width="1337" height="307" alt="image" src="https://github.com/user-attachments/assets/3e22fe08-ac72-4c30-8f78-fbe05fd37863" />


## Access Details

- **Web Console Port:** 9001 (accessed via the KillerCoda "Traffic / Ports" tab)
- **API Port:** 9000 (used by S3-compatible clients/SDKs to talk to the server)
- **Bucket Created:** `client-photos`

## Explanation of the `-e` (Environment Variable) Flags

- `-e "MINIO_ROOT_USER=cloudadmin"` sets the administrator username used to log in to the MinIO console. Environment variables let you configure the container at startup without baking credentials into the image itself.
- `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` sets the administrator password paired with that username. Together, these two variables are how MinIO knows what credentials to require for console and API access — the same pattern most containerized services use to inject configuration/secrets at runtime instead of hardcoding them.

## Screenshots

- <img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/c4f7d05a-d70c-4af4-ab96-a1e4e3750fab" />

` — terminal showing the container running.

- <img width="1913" height="1015" alt="image" src="https://github.com/user-attachments/assets/6da8fcb7-76b6-4436-b605-abd2bd970367" />

` — MinIO console showing the `client-photos` bucket and uploaded file.

