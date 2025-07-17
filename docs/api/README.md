# API Documentation

Welcome to the Tiation API documentation. This section contains comprehensive API references for all Tiation services.

## 📚 Available APIs

### Core Business APIs

#### [19 Trillion Solution API](./19-trillion-solution-api.md)
Enterprise-grade API for the flagship business solution platform.
- RESTful endpoints
- GraphQL interface
- WebSocket real-time updates

#### [Company Intranet API](./company-intranet-api.md)
Internal portal and employee management API.
- Authentication & Authorization
- Employee Directory
- Resource Management

#### [RiggerConnect API](./riggerconnect-api.md)
Workforce management and job matching API for the rigging industry.
- Job Posting & Matching
- Worker Profiles
- Compliance Tracking

### Infrastructure APIs

#### [Automation Server API](./automation-server-api.md)
Backend automation and workflow orchestration.
- Workflow Management
- Task Scheduling
- Event Processing

#### [Metrics Dashboard API](./metrics-dashboard-api.md)
Business intelligence and analytics API.
- Real-time Metrics
- Historical Data
- Custom Reports

## 🔑 Authentication

All APIs use OAuth 2.0 for authentication. See our [Authentication Guide](../guides/authentication.md) for details.

### Quick Start
```bash
# Get access token
curl -X POST https://api.tiation.com/oauth/token \
  -H "Content-Type: application/json" \
  -d '{
    "client_id": "your_client_id",
    "client_secret": "your_client_secret",
    "grant_type": "client_credentials"
  }'
```

## 📡 Base URLs

| Environment | Base URL |
|-------------|----------|
| Production | `https://api.tiation.com/v1` |
| Staging | `https://api-staging.tiation.com/v1` |
| Development | `https://api-dev.tiation.com/v1` |

## 🚦 Rate Limiting

- **Standard**: 1000 requests per hour
- **Premium**: 10,000 requests per hour
- **Enterprise**: Custom limits

## 📖 Response Format

All API responses follow a consistent format:

```json
{
  "success": true,
  "data": {
    // Response data
  },
  "meta": {
    "timestamp": "2025-07-17T00:00:00Z",
    "version": "1.0.0"
  }
}
```

## 🛠️ SDKs & Tools

Official SDKs are available for:
- [JavaScript/TypeScript](https://github.com/tiation/tiation-js-sdk)
- [Python](https://github.com/tiation/tiation-python-sdk)
- [Go](https://github.com/tiation/tiation-go-sdk)
- [Java](https://github.com/tiation/tiation-java-sdk)

## 📚 Additional Resources

- [API Best Practices](../guides/api-best-practices.md)
- [Error Handling Guide](../guides/error-handling.md)
- [Webhook Documentation](./webhooks.md)
- [GraphQL Schema](./graphql-schema.md)

## 🆘 Support

- **Developer Forum**: [forum.tiation.dev](https://forum.tiation.dev)
- **API Status**: [status.tiation.com](https://status.tiation.com)
- **Support Email**: tiatheone@protonmail.com

---

*For detailed endpoint documentation, select an API from the list above.*
