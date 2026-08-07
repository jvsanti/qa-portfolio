# API Testing — Postman: AirportGap API

Created and ran Postman requests against the AirportGap REST API, with scripted assertions.

**Requests created:**
- `GET /airports` — list all airports
- `GET /airports/:id` — get a specific airport (Reykjavik) by ID

**Test script (Tests tab), both assertions passing:**

```javascript
pm.test('Response body contains an airport name, country name, and timezone keys', () => {
  pm.response.to.have.jsonBody('data.attributes.name')
    .and.to.have.jsonBody('data.attributes.country')
    .and.to.have.jsonBody('data.attributes.timezone');
});

pm.test("It's Iceland!", () => {
  pm.expect(pm.response.text()).to.include("Iceland");
});
```

Both tests passed against the live API response.
