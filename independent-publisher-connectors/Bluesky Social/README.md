# Bluesky API Connector

This custom connector allows Power Platform apps to interact with Bluesky's API, supporting operations for managing feeds, conversations, notifications, video uploads, and account data.

## Supported Endpoints

To use this connector, you will need:

- **A Bluesky account.
- **API access to Bluesky with App Password.
- **Obtaining Credentials
- **Go to the Bluesky Developer Portal.
- **Register your App Password in Settings.

## Supported Operations

- **This connector includes the following operations:

### Feed Endpoints

- **GET /app.bsky.feed.getTimeline — Retrieve a user's timeline posts.
- **GET /app.bsky.feed.getFeed — Retrieve posts from a specific feed or tag.
- **GET /app.bsky.feed.searchPosts — Search for posts matching a query.
- **GET /app.bsky.feed.getActorFeeds — Retrieve feeds posted by a specific actor.
- **GET /app.bsky.feed.getActorLikes — Retrieve posts liked by a specific actor.
- **GET /app.bsky.feed.getAuthorFeed — Retrieve posts from a specific author's feed.
- **GET /app.bsky.feed.getFeedGenerator — Retrieve a generated feed for a user.
- **GET /app.bsky.feed.getFeedGenerators — Retrieve metadata about all feed generators.
- **GET /app.bsky.feed.getFeedSkeleton — Retrieve a minimal skeletal version of a feed.
- **GET /app.bsky.feed.getListFeed — Retrieve posts from a specific list.
- **GET /app.bsky.feed.getPosts — Retrieve a list of specific posts by their IDs.
- **GET /app.bsky.feed.getPostThread — Retrieve the thread of posts related to a specific post.
- **GET /app.bsky.feed.getLikes — Retrieve users who liked a specific post.
- **GET /app.bsky.feed.getQuotes — Retrieve posts that quote a specific post.
- **GET /app.bsky.feed.getRepostedBy — Retrieve users who reposted a specific post.
- **GET /app.bsky.feed.getSuggestedFeeds — Retrieve suggested feeds for the user.
- **POST /app.bsky.feed.sendInteractions — Send interactions (like or repost) for a post.

### Actor Endpoints

- **GET /app.bsky.actor.getPreferences — Retrieve the user's preferences.
- **GET /app.bsky.actor.getProfile — Retrieve the profile of a specific user.
- **GET /app.bsky.actor.getProfiles — Retrieve multiple user profiles.
- **GET /app.bsky.actor.getSuggestions — Retrieve account suggestions for the user.
- **POST /app.bsky.actor.putPreferences — Update the user's preferences.
- **GET /app.bsky.actor.searchActors — Search for user accounts by query.
- **GET /app.bsky.actor.searchActorsTypeahead — Retrieve search suggestions for user accounts.

### Graph Endpoints

- **GET /app.bsky.graph.getActorStarterPacks — Retrieve starter packs of accounts for a new user.
- **GET /app.bsky.graph.getKnownFollowers — Get followers known to the authenticated user.
- **GET /app.bsky.graph.getFollowers — Retrieve a list of followers for a user.
- **GET /app.bsky.graph.getFollows — Retrieve users followed by a specific user.
- **GET /app.bsky.graph.getBlocks — Retrieve users blocked by the authenticated user.
- **GET /app.bsky.graph.getList — Retrieve a specific list of users.
- **GET /app.bsky.graph.getLists — Retrieve all lists for the authenticated user.
- **GET /app.bsky.graph.getListBlocks — Retrieve users blocked within a specific list.
- **GET /app.bsky.graph.getListMutes — Retrieve muted lists for the authenticated user.
- **GET /app.bsky.graph.getMutes — Retrieve muted users.
- **GET /app.bsky.graph.getRelationships — Retrieve relationships between the authenticated user and specified accounts.
- **GET /app.bsky.graph.getStarterPack — Retrieve a single starter pack for a new user.
- **GET /app.bsky.graph.getStarterPacks — Retrieve all starter packs for new users.
- **GET /app.bsky.graph.getSuggestedFollowsByActor — Retrieve suggested accounts to follow, filtered by an actor.
- **POST /app.bsky.graph.muteActor — Mute a specific actor.
- **POST /app.bsky.graph.unmuteActor — Unmute a specific actor.
- **POST /app.bsky.graph.muteActorList — Mute a specific list of actors.
- **POST /app.bsky.graph.unmuteActorList — Unmute a specific list of actors.
- **POST /app.bsky.graph.muteThread — Mute an entire thread of posts.
- **POST /app.bsky.graph.unmuteThread — Unmute an entire thread of posts.

### Labeler Endpoints

- **GET /app.bsky.labeler.getServices — Retrieve the list of labeler services available to the user.

### Notification Endpoints

- **GET /app.bsky.notification.getUnreadCount — Retrieve the count of unread notifications.
- **GET /app.bsky.notification.listNotifications — List notifications for the authenticated user.
- **POST /app.bsky.notification.putPreferences — Update notification preferences.
- **POST /app.bsky.notification.registerPush — Register for push notifications.
- **POST /app.bsky.notification.updateSeen — Mark notifications as seen.

### Video Endpoints

- **GET /app.bsky.video.getJobStatus — Retrieve the status of a video upload job.
- **GET /app.bsky.video.getUploadLimits — Retrieve the video upload limits for the user.
- **POST /app.bsky.video.uploadVideo — Upload a video file.

### Unspecced Endpoints

- **POST /app.bsky.unspecced.uploadBlob — Upload a binary blob to the user's account.
- **GET /app.bsky.unspecced.getBlob — Retrieve a binary blob from the user's account.


### Authentication

- **TBD - In progress

### How to Use

Each endpoint has specific parameters (such as user IDs, query strings, or result limits) that need to be configured as per the endpoint's requirements.

- **Authenticate: Start by authenticating with your Bluesky credentials.
- **Choose Endpoint: Select the desired endpoint, such as retrieving a feed or listing notifications.
- **Set Parameters: Provide the required parameters like user IDs, limits, or query strings.
- **Execute Request: Run the request to retrieve data or perform actions within your Power Platform app.

### Example Use Cases

- **Retrieve User Feed: Get posts from a user's timeline or feed to display in your app.
- **Search for Posts: Use a search query to find posts matching user input.
- **Manage Mutes and Blocks: Allow users to manage their mutes and blocks efficiently.
- **Send Notifications: Keep users informed with real-time notifications.
- **Upload Media: Allow users to upload and manage videos or blobs directly.

### Contact

- **dan.romano@swolcat.com or torin@imp.sh (original owner)

