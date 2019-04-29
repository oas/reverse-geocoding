🌍 Reverse Geocoding powered by OpenStreetMap and Elasticsearch

# Elasticsearch

## Mapping
```json
{
  mappings: {
    cities: {
      properties: {
        city: {
          type: "string"
        },
        state: {
          type: "string"
        },
        country: {
          type: "string"
        },
        location: {
          type: "geo_shape",
          precision: "5km", // Level: 5
        }
      }
    }
  }
}
```
