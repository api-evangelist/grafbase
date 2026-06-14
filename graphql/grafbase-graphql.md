# Grafbase GraphQL API

Grafbase provides a GraphQL-based Management API that powers the Grafbase Dashboard and enables programmatic control of all platform resources. The API exposes queries and mutations covering organizations, projects (graphs), branches, subgraph publishing, schema checks, schema proposals, deployments, extensions, access tokens, team management, analytics, and observability data. It follows the Relay connection specification for pagination and uses a union-based error-handling pattern where mutation payloads are unions of success and error types.

Authentication uses Bearer tokens passed in the `Authorization` header. Tokens are scoped to either a user or an account and can optionally be further restricted to specific graphs. Tokens are obtained from the Grafbase Dashboard under Security Settings and are managed programmatically through the `accessTokenCreate` and `accessTokenDelete` mutations. The API uses introspection and can be explored with any GraphQL client such as GraphiQL, Postman, or Insomnia.

The API is self-described as always evolving and may introduce breaking changes at any point. It is designed primarily for internal use by the Grafbase CLI and Dashboard, though it is publicly accessible for automation and integration purposes. Key capabilities include publishing federated subgraph schemas, running schema checks against a branch, managing schema proposals with review workflows, querying deployment history and composition status, retrieving request analytics and tracing data, and administering Slack notifications and team ownership of subgraphs.

**Endpoint:** https://api.grafbase.com/graphql

**Documentation:** https://grafbase.com/docs/platform/api

**References:**
- Documentation: https://grafbase.com/docs/platform/api
- GettingStarted: https://grafbase.com/docs/gateway/installation
