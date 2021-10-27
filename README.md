# Booking and Referrals Targets

BARS Targets repo is responsible to manage targets for multiple environments. In a short description, for each request, this repo will indicate which target to follow.




## Usage

There is a fodler for each environment inside `targets/`. Each folder represents an environment which is defined in the `targets.json` file.

The json file contains a root element `NHSD-ServiceIdentifier` which can't be modified. 

#### Attention
The element `NHS0001`, bellow: 
```json

  "NHS0001": {
    "target": "https://internal-dev.api.service.nhs.uk/bars-mock-receiver-proxy"
  }

```

can't be deleted or modified. This is used as a test target. Tests to the structure of each file will be executed and any change to this element will result in an error message and in a failed deployment. 

#### How to use

You can create more elements inside the root element, e.g:
```json
{
    "NHSD-ServiceIdentifier": {
      "NHS0001": {
        "target": "https://internal-dev.api.service.nhs.uk/bars-mock-receiver-proxy"
      },
       "NHSXXXX": {
        "target": "YOUR-TARGET-URL"
      }
    }
}
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

