# Setup Github Actions with fastlane

# After app is created and setup on App Store Connect

# Data Needed:
APP_STORE_CONNECT_KEY_ID: https://appstoreconnect.apple.com/access/api

APP_STORE_CONNECT_ISSUER_ID: https://appstoreconnect.apple.com/access/api

APP_STORE_CONNECT_PRIVATE_KEY: Download and keep in safe place when first created

FASTLANE_PASSWORD: App-Specific Password for fastlane - https://appleid.apple.com/account/manage

GIT_AUTHORIZATION: <YOUR_GITUSERNAME>:<YOUR_PERSONAL_ACCESS_TOKEN>

IOS_DIST_SIGNING_KEY: Export from keychain then run  base64 -i Certificates.p12 | pbcopy

IOS_DIST_SIGNING_KEY_PASSWORD: Apple developer password

MATCH_PASSWORD: Created when setting up match


APP_STORE_CONNECT_TEAM_ID
DEVELOPER_APP_ID
DEVELOPER_APP_IDENTIFIER
DEVELOPER_PORTAL_TEAM_ID
FASTLANE_APPLE_ID
PROVISIONING_PROFILE_SPECIFIER




# Setup app repo
  automate with fastlane init


# Setup private certificates repo


# Setup Github Secrets for app repo


# Setup fastlane in local app folder with terminal
  fastlane init


# Setup fastlane match
  fastlane match init
    will need url for private secrets repo
  To start from scratch:
    fastlane match nuke development
    fastlane match nude distribution
  Setup provisioning
    fastlane match appstore
    fastlane match development


# Setup fastfile


# Setup Github Action script


# Setup Provisioning on new developer machine

might need to run fastlane-credentials add --username
