# Kovr Public Resources

Public tools and resources for connecting your environment to [Kovr](https://kovr.ai).

## Contents

| Directory | Description |
|-----------|-------------|
| [`resource-collector/`](resource-collector/README.md) | Scans cloud infrastructure (currently AWS) and produces a structured JSON inventory that can be uploaded to Kovr as a source. |
| [`resource-collector/azure/`](resource-collector/azure/README.md) | Terraform and PowerShell scripts that create an Azure service principal for programmatic access. |

## Quick Start

See the [Resource Collector README](resource-collector/README.md) for installation, usage and Docker instructions.

## Configuration

Kovr-specific values are not published in this repository. Kovr provides them, and you supply them as environment variables:

- `KOVR_API_URL`: the Kovr API URL, required to upload results.
- `KOVR_ROLE_ARN`: the Kovr audit role ARN, required for cross-account access.

## Security

- Never commit credentials (AWS keys, Azure client secrets, session tokens) to this repository.
- Use least-privilege, read-only credentials when running the collector.
- To report a security concern, contact your Kovr representative.
