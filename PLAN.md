# Establish an "IPFS identity" which is stored in IPFS and linked permanently via IPNS

## TODO: Keybase-like social proof and Identity for people and organizations

## UI ideas:

* This will have to be an electron app as it will really require an ipfs node runing alongside electron.
* Today it is just being developed in browser to make it simple to run and test
* The included UI in `public/index.html` is merely temporary, just a way to tinker with the `IpfsIdentity` class.
* The UI can construct the `IpfsIdentity` class after checking if there is already an account in the local database (leveldb / IndexedDB) via the `checkForAccount` function.
* The `start` function will return the `IpfsIdentity` instance with:

`const ipid = await start('MyHandleName');`

## Initial thoughts

* Store IPFS id, exported private key, public key, etc in localStorage on device.
* Establish a Public JSON file with public key, image, petname, etc
* Use IPNS to create a permanent link to the IDENTITY json file
* Write public key, petname, bio, IPNS link to IDENTITY, etc to OrbitDB
* Add social proof to IDENTITY json file
* Post a signature of your public key to social media
* Record the links & signatures in IDENTITY json file
* Start with Twitter / Mastodon / Other posted link
* DNS TXT records?
* Allow for other users to VERIFY social proof via public key signature verification
* use PBKDF2 master password to store all private key material / secrets in IDB
* Use a BIP39? master password generator?

### More

* Authentication system a'la OAuth / SSO-type mechanism etc?
* Public, verifiable, web home page
* Secure storage of private key material / IDENTITY json data in hardware wallet?

