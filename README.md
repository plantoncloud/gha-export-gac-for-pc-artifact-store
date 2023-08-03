# Export GAC for Planton Cloud Artifact Store

This GitHub action fetches an Artifact Store Key (reader or writer based on the input) from Planton Cloud and sets it as the `GOOGLE_APPLICATION_CREDENTIALS` environment variable. 

## Inputs

### `planton_cloud_artifact_store_id`

**Required** The ID of the Artifact Store on Planton Cloud.

### `key_type`

**Required** The type of key to fetch. This can be either "reader" or "writer".

## Usage

```yaml
steps:
  - name: Fetch and set Artifact Store Key
    uses: plantoncloud/gha-export-gac-for-pc-artifact-store@main
    with:
      planton_cloud_artifact_store_id: your-artifact-store-id
      key_type: reader # or writer
```

In this example, the `GOOGLE_APPLICATION_CREDENTIALS` environment variable will be set to the reader key for the specified artifact store. If you want the writer key instead, replace `reader` with `writer`.
