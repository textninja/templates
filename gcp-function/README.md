# Example cloud function

This is a starter template for bootstrapping development of Google Cloud Functions. A handful of files, really. It ain't much, but it's honest work!

## Usage

```console
% degit textninja/templates/gcp-function name-for-new-function
```

## Deployment

To deploy this cloud function, use some variation of the commands below. Modify this for your use case or it won't work.

```console
% SERVICE_ACCOUNT=email-for-service-account
% gcloud functions deploy hello-world-function \
  --entry-point=helloWorld \
  --memory=128 \
  --runtime=nodejs16 \
  --ignore-file=.gitignore \
  --trigger-http \
  --max-instances=1 \
  --min-instances=0 \
  --timeout=1 \
  --service-account=$SERVICE_ACCOUNT \
  --set-secrets=/etc/secrets/somesecret=somesecret:latest
```
