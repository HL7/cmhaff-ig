[HL7 Confluence: cMHAFF - Rendered via Common HL7 Toolset (EHR FHIR IG)](https://confluence.hl7.org/pages/viewpage.action?pageId=104575776)

### Convert script

Convert current computable version of the FM (MAX file) to FHIR IG artifacts.
First create and connect to the docker then run all other cmd inside the docker.
```bash
docker run --name=cmhaff-ig -it -v "$(pwd)":/app node:latest /bin/bash
```

```bash
dpkg -i jdk-25_linux-x64_bin.deb # (once)
apt update; apt -y upgrade; apt -y install graphviz jekyll # (once)
cd script
npm install # (once)
# node xlsx2max.js convert -s true -m true -n CMHAFF -i 'CMHAFF migrate to EHR-S FM format 20250130.xlsx' > cmhaff.max
node xlsx2max.js convert -s true -m true -t 1 -n CMHAFF -i 'cMHAFF_STU2_plus_AI_EHR-S_FM_import_20261022.xlsx' > cmhaff.max
node max2fhir.js
```

# Generate the IG (will also run Sushi)
```bash
./_updatePublisher.sh
./_genonce.sh
```

# Antigravity

```bash
curl -fsSL https://antigravity.google/cli/install.sh | bash
cd _local # (anders gaat hij allemaal IG files lezen...)
```
> Make a plan to rewrite all lines in @criteria.txt in the format: "The app {optionality} {verb} ..."
> Optionality is one of SHALL, SHOULD, MAY, SHALL NOT
> The lines can be prefixed with a condition "IF ... THEN the app {optionality} {verb} ...".
> Don't use git.