# cmhaff-ig

https://confluence.hl7.org/display/MH/cMHAFF+EHR-S+FM+FHIR-ized+IG

# Create and Setup Docker Image (prebuild)
```
> docker run --rm -it -v $(pwd):/home/publisher/ig hl7fhir/ig-publisher-base:latest
```

# Generate the IG (will also run Sushi)
```
@> _updatePublisher.sh
@> _genonce.sh
```
