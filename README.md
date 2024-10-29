# `rearm-get-version`

## About
This action uses the Rearm CLI, [`rearm`](https://github.com/rearmio/rearm), to get the version.

## Usage

Get the version info:

```yaml
steps:
- uses: rearmio/rearm-get-version@1.4
  with:
    rearm_api_id: <api-id-obtained-from-rearmhub>
    rearm_api_key: <api-key-obtained-from-rearmhub>
```

## Inputs
The actions supports the following inputs:

- `rearm_api_id`: The project API ID obtained from Rearm.
- `rearm_api_key`: The project API Key obtained from Rearm.
- `ci_metadata`: Metadata for CI run (Optional)
- `path`: Path to the relative to root of the repo (default is '.')
- `rearm_project_id`: Project ID in Rearm Hub to obtain version for in case org-wide api key is used (Optional)

## Outputs
The actions produces the following outputs:

- `rearm_full_version`: Full Version for the new release.
- `rearm_short_version`: Short Version for the new release (this is guaranteed to be compatible with container image tag).
- `rearm_build_start`: Recorded build start time.
- `rearm_do_build`: Flag to control if build should continue.
- `rearm_last_commit`: Last recorded commit prior to the new release.
