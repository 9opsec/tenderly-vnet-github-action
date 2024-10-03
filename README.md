# Tenderly Virtual TestNet GitHub Action

## Overview

This repository contains a GitHub Action that sets up a Tenderly Virtual TestNet for blockchain development and testing. It's designed to automate the process of creating a virtual testnet environment, making it easier to test smart contracts and blockchain applications in a controlled setting.

## Purpose

The primary purposes of this GitHub Action are:

1. **Automated TestNet Setup**: Quickly create a Tenderly Virtual TestNet for each workflow run.
2. **Consistent Testing Environment**: Ensure that all tests are run against a consistent and isolated blockchain environment.
3. **CI/CD Integration**: Seamlessly integrate blockchain testing into your continuous integration and deployment pipelines.
4. **Flexible Configuration**: Allow easy customization of the TestNet parameters to suit different project needs.

## Workflow Details

The workflow is defined in `.github/workflows/test-vnet-action.yml` and includes the following key steps:

1. Checkout the repository
2. Set up the Tenderly TestNet
3. Test the RPC URLs


## Action Inputs

The action accepts the following inputs:

- `access_key`: Tenderly API Access Key (required)
- `project_name`: Tenderly Project Name (required)
- `testnet_slug`: Slug for the Virtual TestNet (default: 'ci_testnet')
- `testnet_name`: Display name for the Virtual TestNet (default: 'CI TestNet')
- `network_id`: Network ID to fork (default: '1')
- `block_number`: Block number to fork from in hex (default: '0x13e772b')


## Action Outputs

The action sets the following environment variables:

- `TENDERLY_TESTNET_ID`: The ID of the created TestNet
- `TENDERLY_ADMIN_RPC_URL`: The Admin RPC URL for the TestNet
- `TENDERLY_PUBLIC_RPC_URL`: The Public RPC URL for the TestNet

## How It Works

1. The action uses the Tenderly API to create a new Virtual TestNet based on the provided inputs.
2. It then extracts the TestNet ID and RPC URLs from the API response.
3. These values are set as environment variables for use in subsequent steps of your workflow.


Make sure to replace `your_project_name`, `your_testnet_slug`, and other values as needed for your project.

## Requirements

- GitHub repository
- Tenderly account and API access key
- Appropriate permissions to run GitHub Actions

## Contributing

Contributions to improve this action are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch for your feature
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

[We need info here, not sure what should be placed]

## Support

For issues and feature requests related to this action, please open an issue in this repository. For general Tenderly support, please refer to the [Tenderly documentation](https://docs.tenderly.co/).


