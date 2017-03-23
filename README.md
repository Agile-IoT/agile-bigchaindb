# Agile-BigchainDB

BigchainDB implementation for Agile IoT gateway


## How to Use:

In index.js, input the following:

- Agile API hostname (example: http://agile.local:8080)
- Device ID
- BigchainDB API endpoint (example: http://localhost:9984/api/v1/)
- Passcode - This is a password for your device (minimum 8 characters)

The password will generate a keypair used to upload readings of all device components to BigchainDB. The publicKey generated from the device's password can be used to lookup the device readings stored in the BigchainDB cluster network using:
GET /api/v1/outputs?public_key={public_key}
