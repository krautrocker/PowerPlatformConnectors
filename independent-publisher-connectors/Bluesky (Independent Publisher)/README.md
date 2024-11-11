# Bluesky API Connector

This custom connector allows Power Platform apps to interact with Bluesky's API, supporting operations for managing feeds, conversations, notifications, video uploads, and account data.

## Supported Endpoints

To use this connector, you will need:
1. A Bluesky account.
2. API access to Bluesky with App Password.

## Obtaining Credentials

1. Go to the [Bluesky Developer Portal](https://docs.bsky.app).
2. Register your App Password in Settings.

## Supported Operations

This connector includes the following operations:

### Feed Endpoints

- **`GET /app.bsky.feed.getTimeline`** - Retrieve a user's timeline posts.
- **`GET /app.bsky.feed.getFeed`** - Retrieve posts from a specific user's or tag's feed.
- **`GET /app.bsky.feed.searchPosts`** - Search for posts that match a query.
- **`GET /app.bsky.feed.getActorFeeds`** - Retrieve feed posts for a specific actor.
- **`GET /app.bsky.feed.getFeedGenerator`** - Retrieve a generated feed for a user based on preferences.
- **`GET /app.bsky.feed.getFeedSkeleton`** - Retrieve a skeletal version of a feed with minimal content.
- **`GET /app.bsky.feed.getPosts`** - Retrieve a list of specific posts by their IDs.
- **`GET /app.bsky.feed.getLikes`** - Retrieve a list of users who liked a specified post.
- **`GET /app.bsky.feed.getQuotes`** - Retrieve a list of posts that quote a specific post.
- **`GET /app.bsky.feed.getSuggestedFeeds`** - Retrieve a list of suggested feeds for the authenticated user.
- **`GET /app.bsky.feed.getRepostedBy`** - Retrieve a list of users who reposted a specific post.
- **`GET /app.bsky.feed.describeFeedGenerator`** - Retrieve metadata about the feed generator, including supported types and limits.
- **`POST /app.bsky.feed.sendInteractions`** - Send an interaction (like or repost) for a specified post.

### Actor Endpoints

- **`GET /app.bsky.actor.getPreferences`** - Retrieve a user's preferences.
- **`GET /app.bsky.actor.getSuggestions`** - Retrieve a list of account suggestions for a user.
- **`GET /app.bsky.actor.searchActors`** - Search for user accounts by query.
- **`GET /app.bsky.actor.exportAccountData`** - Export account data for the authenticated user.

### Video Endpoints

- **`GET /app.bsky.video.getUploadLimits`** - Retrieve video upload limits, including file size and duration.

### Conversation Endpoints

- **`GET /chat.bsky.convo.listConvos`** - List conversations for the authenticated user.
- **`GET /chat.bsky.convo.getConvo`** - Retrieve details about a specific conversation.
- **`POST /chat.bsky.convo.muteConvo`** - Mute a conversation for a specific user.
- **`POST /chat.bsky.convo.leaveConvo`** - Leave a specific conversation.
- **`POST /chat.bsky.convo.sendMessage`** - Send a message within a conversation.

### Notification Endpoints

- **`GET /app.bsky.notification.listNotifications`** - Retrieve notifications for the authenticated user.

### Graph Endpoints

- **`GET /app.bsky.graph.getKnownFollowers`** - Retrieve a list of known followers for a user.
- **`GET /app.bsky.graph.getRelationships`** - Retrieve relationships for a specified user.
- **`GET /app.bsky.graph.getStarterPack`** - Retrieve a recommended list of users for new users.
- **`GET /app.bsky.graph.getStarterPacks`** - Retrieve multiple starter packs containing recommended users.
- **`GET /app.bsky.graph.getListBlocks`** - Retrieve a list of users blocked by a specified user.
- **`GET /app.bsky.graph.getBlocks`** - Retrieve a list of users blocked by the authenticated user.

## Authentication

The connector uses **Basic Authentication** with an app password. Ensure you have the correct credentials before using the connector.

## How to Use

Each endpoint has specific parameters (such as user IDs, query strings, or limits for results) that need to be configured as per the endpoint's requirements.

1. **Authenticate**: Start by authenticating with your Bluesky credentials.
2. **Choose Endpoint**: Select the desired endpoint, e.g., to retrieve a feed, list conversations, or get notifications.
3. **Set Parameters**: Provide required parameters such as user IDs, limits, or query strings.
4. **Execute Request**: Run the request to retrieve data or perform the action within your Power Platform app.

## Example Use Cases

- **Retrieve User Feed**: Get posts from a user's timeline or feed to display in your app.
- **Search for Posts**: Use a search query to find relevant posts matching user input.
- **Export Account Data**: Retrieve all account data for backup or reporting.
- **List Notifications**: Display recent notifications to keep users informed.
- **Manage Conversations**: List, mute, leave, or retrieve details about user conversations.
- **Send Interactions**: Allow users to like or repost content directly from your app.

This connector enables a wide range of integrations between Bluesky and Power Platform apps, providing rich functionality for enhanced user experiences.
