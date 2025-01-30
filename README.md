https://confluence.hl7.org/display/MH/cMHAFF+EHR-S+FM+FHIR-ized+IG

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

### TODO

* depend on base ehr profiles; now copied from ehrsfm-ig in this IG and changed to canonical of this IG
    * we need these profiles because there are validation rules in there!
* check all criteria with latest CMHAFF publication
* copy all narrative content into the markdown files (maybe separate files for large chapters) and create png for all images
* there is a lot of narrative added e.g. "Implementation Guidance" chapters or "Related Regulations and Standards"
  where should that "sit" at section/header/function level?