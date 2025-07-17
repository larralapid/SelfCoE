# API Documentation

This section contains the API documentation for SelfCoE.

## Overview

SelfCoE provides a RESTful API for programmatic access to the platform's features.

## Base URL

- **Development**: `http://localhost:7007/api`
- **Production**: `https://your-instance.com/api`

## Authentication

SelfCoE uses token-based authentication. Include your token in the Authorization header:

```bash
Authorization: Bearer YOUR_TOKEN
```

## Endpoints

### Catalog API

#### Get All Entities
```
GET /catalog/entities
```

Returns a list of all catalog entities.

**Response:**
```json
{
  "items": [
    {
      "apiVersion": "backstage.io/v1alpha1",
      "kind": "Component",
      "metadata": {
        "name": "example-service",
        "namespace": "default"
      },
      "spec": {
        "type": "service",
        "lifecycle": "production",
        "owner": "team-a"
      }
    }
  ]
}
```

#### Get Entity by Name
```
GET /catalog/entities/by-name/{kind}/{namespace}/{name}
```

Returns a specific entity by its name.

**Parameters:**
- `kind`: The entity kind (e.g., Component, System, API)
- `namespace`: The entity namespace (default: "default")
- `name`: The entity name

### Scaffolder API

#### List Templates
```
GET /scaffolder/v2/templates
```

Returns available scaffolding templates.

#### Create from Template
```
POST /scaffolder/v2/tasks
```

Creates a new project from a template.

**Request Body:**
```json
{
  "templateRef": "template:default/example-template",
  "values": {
    "name": "my-new-service",
    "description": "A new service"
  }
}
```

### TechDocs API

#### Get Documentation
```
GET /techdocs/static/docs/{namespace}/{kind}/{name}
```

Returns documentation for a specific entity.

## Error Handling

The API uses standard HTTP status codes:

- `200` - Success
- `400` - Bad Request
- `401` - Unauthorized
- `403` - Forbidden
- `404` - Not Found
- `500` - Internal Server Error

Error responses include a message field:

```json
{
  "error": {
    "name": "NotFoundError",
    "message": "Entity not found"
  }
}
```

## Rate Limiting

API requests are rate-limited to prevent abuse:

- **Authenticated users**: 1000 requests per hour
- **Unauthenticated users**: 100 requests per hour

Rate limit headers are included in responses:

```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 999
X-RateLimit-Reset: 1640995200
```

## SDK and Libraries

### JavaScript/TypeScript
```bash
npm install @backstage/catalog-client
```

```typescript
import { CatalogApi } from '@backstage/catalog-client';

const catalogApi = new CatalogApi({
  baseUrl: 'http://localhost:7007/api'
});

const entities = await catalogApi.getEntities();
```

### Python
```bash
pip install requests
```

```python
import requests

response = requests.get(
    'http://localhost:7007/api/catalog/entities',
    headers={'Authorization': 'Bearer YOUR_TOKEN'}
)
entities = response.json()
```

### cURL Examples

```bash
# Get all entities
curl -H "Authorization: Bearer YOUR_TOKEN" \
     http://localhost:7007/api/catalog/entities

# Get specific entity
curl -H "Authorization: Bearer YOUR_TOKEN" \
     http://localhost:7007/api/catalog/entities/by-name/component/default/my-service
```

## OpenAPI Specification

The complete API specification is available in OpenAPI format:

- [OpenAPI 3.0 Specification](openapi.json)
- [Swagger UI](swagger/)

## Support

For API support and questions:

- [GitHub Issues](https://github.com/larralapid/SelfCoE/issues)
- [API Documentation](https://larralapid.github.io/SelfCoE/api/)
- [Backstage API Docs](https://backstage.io/docs/features/software-catalog/software-catalog-api)