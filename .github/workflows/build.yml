name: Build Madeira iPhone package (branch validation)

on:
  push:
    branches:
      - main
  workflow_dispatch:
    inputs:
      ref:
        description: 'Commit or branch to build'
        required: false
        type: string
        default: 'claude/dazzling-mccarthy-7x4b15'
      configuration:
        description: 'Xcode configuration'
        type: choice
        options: [Debug, Release]
        default: Debug

permissions:
  contents: read
  actions: write

jobs:
  build:
    uses: ./.github/workflows/ios-app.yml
    with:
      ref: ${{ inputs.ref }}
      configuration: ${{ inputs.configuration }}
