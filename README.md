🌍 Reverse Geocoding powered by OpenStreetMap and Elasticsearch

# Elasticsearch

## Mapping
The current version stores all cities worldwide. For this purpose, the following information is stored: the name of the city, the name of the state, the name of the country and the bounding box defined by a polygon:
```js
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
