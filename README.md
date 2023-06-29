# Upload to CPAN

GitHub action to upload a release to CPAN with no dependency on `cpan-upload`.

This action is written in typescript, using its own pause client.

```yaml
- name: Upload release to CPAN
  uses: perl-action/cpan-upload@stable
  with:
    username: PAUSE_USERNAME
    password: ${{ secrets.PAUSE_PASSWORD }}
    file: DISTNAME.VERSION.tar.gz
```

## Using cpan-upload in a workflow

This is an example workflow using the cpan-upload action.

```yaml
```

## Inputs

### `directory`

A directory name to store the uploaded file in on PAUSE. This is optional

### `file`

This is the name of the local file to upload. This is a required input.

### `filename`

The name of the file to store the upload as on PAUSE. This is optional.

### `password`

The PAUSE password for the account with specified username. This is required input and it is recommended that this uses a stored secret.

### `username`

Your PAUSE username. This is a required input.

## Outputs

### `download-url`

The URL from which the released file may be downloaded from.

### `metacpan-url`

The URL for the release.