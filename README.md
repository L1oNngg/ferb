# API Documentation: Update Customer Information

## PATCH `/customer/:username`

### Description
This endpoint allows authorized users to update customer information. It supports updates for fields such as `name`, `email`, and `phone`. Access is restricted based on user roles:
- **Admin** and **Manager**: Can update any customer's information.
- **Customer**: Can update only their own information.

---

### Request Details

#### URL Parameters
- `:username` (string): The username of the customer to update.

#### Headers
- **Authorization**: A valid token is required for authentication and role-based access.

#### Request Body
The request body should contain the fields to update. All fields are optional. Example:
```json
{
  "name": "Updated Name",
  "email": "updated.email@example.com",
  "phone": "1234567890"
}
