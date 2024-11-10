# Bluesky API (Independent Publisher)

The Bluesky API custom connector allows Power Platform users to interact with the Bluesky platform. With this connector, you can retrieve user timelines, create new posts, and fetch profile details, enabling seamless integration with Power Apps and Power Automate.

## Publisher: Independent Publisher

## Prerequisites

To use this connector, you will need:
1. A Bluesky account.
2. API access to Bluesky with OAuth 2.0 credentials (Client ID and Client Secret).

## Obtaining Credentials

1. Go to the [Bluesky Developer Portal](https://docs.bsky.app).
2. Register your application to obtain the Client ID and Client Secret.
3. Set up the OAuth 2.0 settings as follows:
   - **Authorization URL**: `https://bsky.app/oauth/authorize`
   - **Token URL**: `https://bsky.app/oauth/token`
   - **Redirect URL**: Specify a redirect URL (e.g., `https://global.consent.azure-apim.net/redirect`) that allows the Power Platform to complete the OAuth 2.0 flow.

## Supported Operations

This connector includes the following operations:

### 1. Get User Timeline
- **Description**: Retrieves a list of posts from a specified user's timeline.
- **Endpoint**: `GET /xrpc/app.bsky.feed.getTimeline`
- **Parameters**:
  - `user` (required): The username or user ID for the timeline.
  - `limit` (optional): The number of posts to retrieve.

### 2. Create a New Post
- **Description**: Posts a new status update to the user's feed.
- **Endpoint**: `POST /xrpc/app.bsky.feed.post`
- **Body Parameters**:
  - `content`: The text content of the post (maximum 280 characters).
  - `attachments` (optional): Array of URLs for any media attachments.

### 3. Get User Profile
- **Description**: Retrieves profile information for a specified user.
- **Endpoint**: `GET /xrpc/app.bsky.actor.getProfile`
- **Parameters**:
  - `user` (required): The username or user ID of the profile to retrieve.

## Testing the Connector

1. **Custom Connector Test Interface**:
   - Go to the Power Platform environment where you have created the Bluesky custom connector.
   - Open the connector and navigate to the "Test" tab.
   - Select or create a connection and run test requests for each operation to verify the connector's functionality.

2. **Testing in a Flow**:
   - Create a new Flow in Power Automate.
   - Add an action using the Bluesky connector for each operation (`Get User Timeline`, `Create Post`, `Get User Profile`).
   - Run the Flow and verify the results.
   - Take screenshots of successful runs for submission.

## Known Issues and Limitations

- **Rate Limits**: Bluesky API imposes rate limits on requests. Ensure you stay within the allowed limits to avoid throttling.
- **OAuth Expiration**: The OAuth token may expire after a certain period. Implement token refresh logic as needed.

## Deployment Instructions

1. **Create the Connector**:
   - Navigate to Power Apps or Power Automate, and select "Custom Connectors".
   - Choose "Import an OpenAPI file" and upload the `apiDefinition.swagger.json` file.
   - Configure OAuth 2.0 settings as described above.
   - Save and test the connector.

2. **Validate the Connector**:
   - Use the `paconn validate` command to ensure there are no issues with the `apiDefinition.swagger.json` file.

3. **Publish the Connector**:
   - After successful testing, publish the connector and submit it as a PR in the [PowerPlatformConnectors GitHub repository](https://github.com/microsoft/PowerPlatformConnectors) with the PR title `Bluesky API (Independent Publisher)`.

## Additional Notes

- **Brand Colors**: If submitting as a certified connector, ensure that `apiProperties.json` does not use invalid brand colors like `#007ee5` or `#ffffff`.
- **API Documentation**: For more details on available endpoints, visit the [Bluesky API documentation](https://docs.bsky.app).

## Disclaimer

This connector was created by an Independent Publisher and is not affiliated with or endorsed by Bluesky.

