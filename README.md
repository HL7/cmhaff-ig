[HL7 Confluence: cMHAFF - Rendered via Common HL7 Toolset (EHR FHIR IG)](https://confluence.hl7.org/pages/viewpage.action?pageId=104575776)

### Convert script

Convert current computable version of the FM (MAX file) to FHIR IG artifacts.
```
> docker run --name=cmhaff-ig -it -v "$(pwd)":/app node:latest /bin/bash
@> (once) dpkg -i jdk-23_linux-x64_bin.deb
@> (once) apt update; apt -y upgrade; apt -y install graphviz jekyll
@> cd script
@> (once) npm install
@> node xlsx2max.js convert -s true -m true -n CMHAFF -i 'CMHAFF migrate to EHR-S FM format 20250130.xlsx' > cmhaff.max
@> node max2fhir.js
```

# Generate the IG (will also run Sushi)
```
@> ./_updatePublisher.sh
@> ./_genonce.sh
```