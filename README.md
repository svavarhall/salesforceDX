# SFDX  Demo App

## List of useful commands

Creating a project:
```
sfdx force:project:create -n nameofproject
```

Creating a scratch org for that project
```
sfdx force:org:create -s -f config/project-scratch-def.json -a nameOfProjectScratch
```

Open the app
```
sfdx force:org:open
```

Assigning a permission set:
```
sfdx force:user:permset:assign -n Geolocation
```
Pulling changes into project:
```
sfdx force:source:pull
```

Example: Exporting data for scratch org testing:
```
sfdx force:data:tree:export -q "SELECT Name, Location__Latitude__s, Location__Longitude__s FROM Account WHERE Location__Latitude__s != NULL AND Location__Longitude__s != NULL" -d ./data
```

Importing that data into a scratch org:
```
sfdx force:data:tree:import --sobjecttreefiles data/Account.json
```


## Resources


## Description of Files and Directories


## Issues


