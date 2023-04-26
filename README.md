# Setup Github Actions with fastlane

### After app is created and setup on App Store Connect

## Data Needed:
If you use the default env names values will be passed automatically for these values

  key_id: ENV["APP_STORE_CONNECT_API_KEY_KEY_ID"],
  issuer_id: ENV["APP_STORE_CONNECT_API_KEY_ISSUER_ID"],
  key_content: ENV["APP_STORE_CONNECT_API_KEY_KEY"]

APP_STORE_CONNECT_KEY_ID: https://appstoreconnect.apple.com/access/api<br>
APP_STORE_CONNECT_ISSUER_ID: https://appstoreconnect.apple.com/access/api<br>
APP_STORE_CONNECT_PRIVATE_KEY: Download and run base64 -i certificate-name.p8 | pbcopy<br>

FASTLANE_PASSWORD: App-Specific Password for fastlane - https://appleid.apple.com/account/manage<br>
MATCH_PASSWORD: Created when setting up match<br>
GIT_AUTHORIZATION: YOUR_GITUSERNAME:YOUR_PERSONAL_ACCESS_TOKEN<br>

IOS_DIST_SIGNING_KEY: Export from keychain then run base64 -i certificate-name.p12 | pbcopy<br>
IOS_DIST_SIGNING_KEY_PASSWORD: Apple developer password<br>

### KEEP ALL CERTIFICATES AND PROFILES IN SAFE PLACE NOT IN REPO

Not needed?
APP_STORE_CONNECT_TEAM_ID<br>
DEVELOPER_APP_ID<br>
DEVELOPER_APP_IDENTIFIER<br>
DEVELOPER_PORTAL_TEAM_ID<br>
FASTLANE_APPLE_ID<br>
PROVISIONING_PROFILE_SPECIFIER<br>



## Setup app repo
  automate with fastlane init


## Setup private certificates repo
  Create a private repo which will hold certificates,
  supply url to fastlane match init

## Setup Github Secrets for app repo
  On the app repo goto settings/secrets/actions
  Setup secrets listed under data needed above


## Setup fastlane in local app folder with terminal
  fastlane init


## Setup fastlane match
  fastlane match init
    will need url for private secrets repo

  To start from scratch:
    fastlane match nuke development
    fastlane match nude distribution

  Setup provisioning
    fastlane match appstore
    fastlane match development


## Setup fastfile


## Setup Github Action script


## Setup Provisioning on new developer machine


## Extras
  Turn off Automatically manage signing
  Select Match Appstore for Provisioning Profile

  Might need to run fastlane-credentials add --username

  To keep build number in sync add to build scheme
  Edit Scheme/Build/Post-actions/New Run Script Action
  cd "${PROJECT_DIR}" ; agvtool bump
  set build setting to app name
