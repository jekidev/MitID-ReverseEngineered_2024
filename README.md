# MitID-ReverseEngineered


https://github.com/Hundter/MitID-ReverseEngineered/assets/9397488/4c4fd48f-6f16-420f-a71a-a7c1d342bc40

## Release background
Digitaliseringstyrelsen [has now enabled an app integrity check on the MitID server side](https://digst.dk/nyheder/nyhedsarkiv/2024/juni/mitid-faar-ekstra-antisvindel-mekanisme/), which enables them to deny this "custom" authenticator from registrering itself.

The risk of supply chain attacks involved in publicising this code has therefore been mitigated, and i hope this release will allow universities like DTU, to evaulate the design of the MitID protocol, furthering danish IT security.

## Features
  - Registering itself as a MitID authenticator (until June 2024)
  - Approving MitID login requests
  - Skips the QR code scan step when logging in to MitID, since that is not a server-side requirement in the protocol
  - Generating activation tokens used for creating new authenticators
  - Revoking itself as an authenticator
  - Updating the authenticator information stored on the server side



The keys that this authenticator generates, an RSA key and an ECC key, are stored unsafely in a json file for simplicity in this implementation.
In the official MitID Android app, the keys are stored in a BouncyCastle keystore and hardware backed key storage respectively. It is also not possible to even use both of these keys without at least some communication and authentication with the MitID server.
