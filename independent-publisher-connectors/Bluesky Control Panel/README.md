# Bluesky API Connector - Non-App.Bsky Endpoints

This custom connector allows Power Platform apps to interact with Bluesky’s API, supporting operations for managing actors, moderation, labels, identity, synchronization, and administrative controls outside the `app.bsky` namespace.

## Supported Endpoints

To use this connector, you will need:
1. A Bluesky account.
2. API access to Bluesky with an App Password.

## Obtaining Credentials
1. Go to the [Bluesky Developer Portal](https://docs.bsky.app).
2. Register your App Password in Settings.

## Supported Operations

This connector includes the following operations:

#### Actor Endpoints
- **POST /chat.bsky.actor.deleteAccount** – Permanently delete an actor's account and associated data.
- **GET /chat.bsky.actor.exportAccountData** – Export account data for a specific actor.

#### Moderation Endpoints
- **POST /com.atproto.moderation.createReport** – Create a moderation report for actor behavior or content.
- **GET /com.atproto.moderation.getActorMetadata** – Retrieve metadata associated with an actor's moderation status.
- **PUT /com.atproto.moderation.updateActorAccess** – Update access permissions for a specified actor.

#### Label Endpoints
- **GET /com.atproto.label.queryLabels** – Query labels for content or actors.

#### Identity Endpoints
- **POST /com.atproto.identity.updateHandle** – Update the handle associated with an actor's account.
- **GET /com.atproto.identity.getRecommendedDIDCredentials** – Retrieve recommended DID credentials for account verification.

#### Repository Endpoints
- **POST /com.atproto.repo.uploadBlob** – Upload a binary blob to the repository.
- **POST /com.atproto.repo.applyWrites** – Apply multiple writes to the repository.
- **POST /com.atproto.repo.createRecord** – Create a new record in the repository.
- **DELETE /com.atproto.repo.deleteRecord** – Delete a specified record from the repository.
- **GET /com.atproto.repo.describeRepo** – Retrieve metadata about a repository.
- **GET /com.atproto.repo.getRecord** – Retrieve a specific record by ID.
- **POST /com.atproto.repo.importRepo** – Import data into the repository.
- **GET /com.atproto.repo.listMissingBlobs** – List missing blobs in the repository.
- **GET /com.atproto.repo.listRecords** – List all records in a repository.
- **PUT /com.atproto.repo.putRecord** – Update a record in the repository.

#### Synchronization Endpoints
- **GET /com.atproto.sync.getBlob** – Retrieve a specific blob in binary format.
- **GET /com.atproto.sync.getBlocks** – Retrieve binary data blocks by ID.
- **GET /com.atproto.sync.getLatestCommit** – Retrieve the latest commit information for synchronization.
- **GET /com.atproto.sync.getRecord** – Retrieve a specific record as part of sync operations.
- **GET /com.atproto.sync.getRepoStatus** – Get the status of a repository for sync operations.

#### Server Endpoints
- **POST /com.atproto.server.activateAccount** – Activate a new account.
- **POST /com.atproto.server.createAccount** – Create a new account in the system.
- **DELETE /com.atproto.server.deleteAccount** – Permanently delete an account.
- **GET /com.atproto.server.getSession** – Retrieve the current session information.
- **POST /com.atproto.server.updateEmail** – Update the email address for an account.

#### Tools-Ozone Communication Endpoints
- **POST /tools.ozone.communication.createTemplate** – Create a communication template.
- **DELETE /tools.ozone.communication.deleteTemplate** – Delete a communication template by ID.
- **GET /tools.ozone.communication.listTemplates** – List all communication templates.
- **PUT /tools.ozone.communication.updateTemplate** – Update an existing communication template.

#### Tools-Ozone Moderation Endpoints
- **POST /tools.ozone.moderation.emitEvent** – Emit a moderation event.
- **GET /tools.ozone.moderation.getRecord** – Retrieve a moderation record by ID.
- **GET /tools.ozone.moderation.getRecords** – Retrieve multiple moderation records.
- **GET /tools.ozone.moderation.searchRepos** – Search for repositories based on moderation criteria.

#### Tools-Ozone Team Endpoints
- **POST /tools.ozone.team.addMember** – Add a member to a specified team.
- **DELETE /tools.ozone.team.deleteMember** – Remove a member from a specified team.
- **GET /tools.ozone.team.listMembers** – List all members of a specified team.
- **PUT /tools.ozone.team.updateMember** – Update information for a team member.

All other endpoints not listed can be found here (non-app.bsky): https://docs.bsky.app/docs/category/http-reference


### Authentication
All endpoints require an `Authorization` header with a bearer token, except where explicitly noted.

### Example Authorization Header

{
  "Authorization": "Bearer <your_access_token>"
}
