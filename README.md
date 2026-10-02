# MitID-ReverseEngineered


https://github.com/jekidev/MitID-ReverseEngineered_2024

The risk of supply chain attacks involved in publicising this code has therefore been mitigated, and i hope this release will allow universities like DTU, to evaulate the design of the MitID protocol, furthering danish IT security.

## Features
  - Registering itself as a MitID authenticator (until June 2024)
  - Approving MitID login requests
  - Skips the QR code scan step when logging in to MitID, since that is not a server-side requirement in the protocol
  - Generating activation tokens used for creating new authenticators
  - Revoking itself as an authenticator
  - Updating the authenticator information stored on the server side

