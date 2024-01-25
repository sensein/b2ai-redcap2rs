# Converting bridge2ai redcap to reproschema

This repository contains the version-controlled implementation of the Bridge2AI ReproSchema, converted from REDCap data dictionaries, using the [`redcap2reproschema`](https://github.com/ReproNim/reproschema-py#redcap2reproschema-usage) tool

## Conversion Process

For each REDCap data dictionary version, we did the following

1. Convert to reproschema format

Install the tool `reproschema-py` 
```
git clone https://github.com/ReproNim/reproschema-py.git
cd reproschema-py
pip install -e .
```
Convert the data dictionary
```
reproschema redcap2reproschema [b2ai-redcap-data-dictionary.csv] [redcap2rs.ymal]
```

2. Git add and commit

Add and commit the newly converted reproschema
```
git add .
git commit -m "converted b2ai redcap data dictionary version xx to reproschema"
```

3. Version tagging

After committing the changes, each version was tagged to mark the release point in the repository's history. For example:
```
git tag -a v1.0-redcap2rs-conversion -m "redcap data dictionary version 1.0 to reproschema"
```

4. Git push

Push the current tag to remote
```
git push
```