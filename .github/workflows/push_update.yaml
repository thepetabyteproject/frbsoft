name: Update list

on: [push]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.8
      uses: actions/setup-python@v1
      with:
        python-version: 3.8
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install best-of
    - name: update-best-of-list
      uses: best-of-lists/best-of-update-action@v0.5.1
      with:
        github_key: ${{ secrets.GITHUB_TOKEN }}
        projects_file: "./projects.yaml"
