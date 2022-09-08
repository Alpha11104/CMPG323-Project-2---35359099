# CMPG323-Project-2---35359099
### Demo Accounts for login
The following accounts have been created in the database for use for the marker.
#### Role User:
```JSON
{
  "username": "user",
  "password": "P@ssword123"
}
```
#### Role Admin:
```JSON
{
  "username": "admin",
  "password": "P@ssword123"
}
```
---
### **Populated Data**
The following entries have been added in the database for ease of the marker.
#### Categories:
```JSON
[
  {
    "categoryId": "233fcb41-9da0-4ae1-9ab5-a79a60807bd4",
    "categoryName": "Stationary",
    "categoryDescription": "Category for devices that can not be easily moved.",
    "dateCreated": "2022-09-06T15:36:32.03"
  },
  {
    "categoryId": "5dca355f-7456-4db3-8b47-e4c121661398",
    "categoryName": "Mobile",
    "categoryDescription": "Category for mobile devices.",
    "dateCreated": "2022-09-06T15:36:32.03"
  }
]
```
#### Zones:
```JSON
[
  {
    "zoneId": "f5a95f6b-f48e-49c8-b0ee-35d68c7b1b82",
    "zoneName": "Break Room",
    "zoneDescription": "The break room for the company",
    "dateCreated": "2022-09-06T15:40:21.6"
  },
  {
    "zoneId": "149a1062-ac8c-4a32-9ff2-517d5f70c33b",
    "zoneName": "Meeting Room",
    "zoneDescription": "The meeting room for the company",
    "dateCreated": "2022-09-06T15:40:21.6"
  },
  {
    "zoneId": "dbbc525f-228d-47b2-b99b-719d7cefae94",
    "zoneName": "Main Office",
    "zoneDescription": "The main office for the company",
    "dateCreated": "2022-09-06T15:40:21.6"
  }
]
```
#### Devices:
```JSON
[
  {
    "deviceId": "a6221766-0d6a-42ff-b5cc-2c636a95b274",
    "deviceName": "Laptop 3",
    "categoryId": "5dca355f-7456-4db3-8b47-e4c121661398",
    "zoneId": "dbbc525f-228d-47b2-b99b-719d7cefae94",
    "status": "Online",
    "isActvie": true,
    "dateCreated": "2022-09-07T17:00:34.277"
  },
  {
    "deviceId": "060915cb-ddb0-4d58-a451-57b35ac26b07",
    "deviceName": "Laptop 2",
    "categoryId": "5dca355f-7456-4db3-8b47-e4c121661398",
    "zoneId": "dbbc525f-228d-47b2-b99b-719d7cefae94",
    "status": "Online",
    "isActvie": true,
    "dateCreated": "2022-09-07T17:00:34.277"
  },
  {
    "deviceId": "57d1f097-4d00-4bc6-95f4-59eedbcf7fe1",
    "deviceName": "Smart Vending Machine",
    "categoryId": "233fcb41-9da0-4ae1-9ab5-a79a60807bd4",
    "zoneId": "f5a95f6b-f48e-49c8-b0ee-35d68c7b1b82",
    "status": "Broken :(",
    "isActvie": true,
    "dateCreated": "2022-09-08T12:23:06.26"
  },
  {
    "deviceId": "6047e4fa-5a36-4e23-bab8-5a6b6e7ae43f",
    "deviceName": "Smart Projector",
    "categoryId": "233fcb41-9da0-4ae1-9ab5-a79a60807bd4",
    "zoneId": "149a1062-ac8c-4a32-9ff2-517d5f70c33b",
    "status": "Online",
    "isActvie": true,
    "dateCreated": "2022-09-06T15:45:43.98"
  },
  {
    "deviceId": "1547dfc2-35a9-43de-8e11-6f060f19337d",
    "deviceName": "Laptop 1",
    "categoryId": "5dca355f-7456-4db3-8b47-e4c121661398",
    "zoneId": "dbbc525f-228d-47b2-b99b-719d7cefae94",
    "status": "Online",
    "isActvie": true,
    "dateCreated": "2022-09-07T17:00:34.277"
  },
  {
    "deviceId": "a0dc1d7a-8c71-40d3-924e-70f011c2bd72",
    "deviceName": "Printer",
    "categoryId": "233fcb41-9da0-4ae1-9ab5-a79a60807bd4",
    "zoneId": "dbbc525f-228d-47b2-b99b-719d7cefae94",
    "status": "Online",
    "isActvie": true,
    "dateCreated": "2022-09-07T17:00:34.277"
  },
  {
    "deviceId": "4353c545-84cc-4c9c-8efe-943d36ea0424",
    "deviceName": "Video Recorder",
    "categoryId": "233fcb41-9da0-4ae1-9ab5-a79a60807bd4",
    "zoneId": "149a1062-ac8c-4a32-9ff2-517d5f70c33b",
    "status": "Online",
    "isActvie": true,
    "dateCreated": "2022-09-07T17:00:34.277"
  },
  {
    "deviceId": "13e9b6cd-4b1b-4302-82cd-aedadb6e8525",
    "deviceName": "Tablet 1",
    "categoryId": "5dca355f-7456-4db3-8b47-e4c121661398",
    "zoneId": "149a1062-ac8c-4a32-9ff2-517d5f70c33b",
    "status": "Online",
    "isActvie": true,
    "dateCreated": "2022-09-07T17:00:34.277"
  }
]
```
---
### **Authentication:**
JWT Bearer Token authentication has been implemented for all routes. You must be logged is as a user to access any GET routes and you must be logged in as an admin to access any POST, PUT or DELETE routes. Please see endpoints documentation for specific route authentication requirements.
### **Auth Flow:**
Login with username and password using route:
`POST: /api/Authenticate/login`
The response object will return a token field. Using the swagger interface copy the token from the response body and prefix the token with Bearer before adding the prefixed token in authorize field in swagger. 
### **Auth Endpoints:**
`POST: /api/Authenticate/login`
#### **Description:** Used to login using a username and password.
#### **Authentication:** None
`POST: /api/Authenticate/register`
#### **Description** Used to register an account with the role of user.
#### **Authentication:** None
`POST: /api/Authenticate/register-admin`
#### **Description** Used to register an account with the role of admin.
#### **Authentication:** Bearer Token with role of admin.
#### **Note:** You must be logged in with an account that has the role of admin in order to create a new account with the role of admin.
---
## **Generated Endpoints:**
### **Categories:**
`GET: /api/Categories`
#### **Description** Returns a list of all categories.
#### **Authentication:** Bearer Token with role of user or admin.

`POST: /api/Categories`
#### **Description** Used to create a new category.
#### **Authentication:** Bearer Token with role of admin.

`GET: /api/Categories/{id}`
#### **Description** Returns a single category matching the id passed through..
#### **Authentication:** Bearer Token with role of user or admin.

`PUT: /api/Categories/{id}`
#### **Description** Used to update the fields of a category based on the id passed through..
#### **Authentication:** Bearer Token with role of admin.

`DELETE: /api/Categories/{id}`
#### **Description** Used to delete a category based on the id passed through.
#### **Authentication:** Bearer Token with role of admin.

### **Zones:**
---
### **Devices:**
`GET: /api/Devices`
#### **Description** Returns a list of all devices.
#### **Authentication:** Bearer Token with role of user or admin.

`POST: /api/Devices`
#### **Description** Used to create a new device.
#### **Authentication:** Bearer Token with role of admin.

`GET: /api/Devices/{id}`
#### **Description** Returns a single device matching the id.
#### **Authentication:** Bearer Token with role of user or admin.

`PUT: /api/Devices/{id}`
#### **Description** Used to update the fields of a device based on the id.
#### **Authentication:** Bearer Token with role of admin.

`DELETE: /api/Devices/{id}`
#### **Description** Used to delete a device based on the id.
#### **Authentication:** Bearer Token with role of admin.
---

### Custom Endpoints:
The followings endpoints were added per rubric requirements. The routes have been documented here for ease of the marker.
### **Categories:**
### `GET: api/Categories/{id}/devices`
#### **Description** Returns a list of devices in a specific category based on the ID that was passed.
#### **Authentication:** Bearer Token with role of user or admin.
```C#
public async Task<ActionResult<IEnumerable<Device>>> GetCategoryDevices(Guid id)
{
    var category = await _context.Category.FindAsync(id);
    if (category == null)
    {
        return NotFound();

    var devices = await _context
        .Device
        .Where(d => d.CategoryId == category.CategoryId)
        .ToListAsync

    return devices;
}
```
### `GET: api/Categories/{id/zone-count`
#### **Description** Returns the number of zones associated with a specific category.
#### **Authentication:** Bearer Token with role of user or admin.
```C#
public async Task<ActionResult<int>> GetCategoryZoneCount(Guid id)
{
    var category = await _context.Category.FindAsync(id);
    if (category == null)
    {
        return NotFound();

    var zoneCount = _context
        .Device
        .Where(d => d.CategoryId == category.CategoryId)
        .Count();

    return zoneCount;
}
```
### `DELETE: api/Zone/private/{id}`
#### **Description** Checks if a Zone exists before deleting it.
#### **Authentication:** Bearer Token with role of admin.
```C#
public async Task<ActionResult<Zone>> AuthDeleteZone(Guid id)
{
    var zone = await _context.Zone.FindAsync(id);
    if (zone == null)
    {
        return NotFound();
    }
    _context.Zone.Remove(zone);
    await _context.SaveChangesAsync():
    return zone;
}
```
---
### **Zones:**
### `GET: api/Zone/{id/devices`
#### **Description** Returns the number of devices associated with a specific zone.
#### **Authentication:** Bearer Token with role of user or admin.
```C#
public async Task<ActionResult<IEnumerable<Device>>> GetDeviceByZoneId(Guid id)
{
    var zone = await _context.Zone.FindAsync(id);

    if (zone == null)
    {
        return NotFound();
    }

    var devices = await _context
        .Device
        .Where(d => d.ZoneId == zone.ZoneId)
        .ToListAsync;

    return devices;
}
```
### `DELETE: api/Zone/private/{id}`
#### **Description** Checks if a Zone exists before deleting it.
#### **Authentication:** Bearer Token with role of admin.
```C#
public async Task<ActionResult<Zone>> AuthDeleteZone(Guid id)
{
    var zone = await _context.Zone.FindAsync(id);
    if (zone == null)
    {
        return NotFound();
    }
    _context.Zone.Remove(zone);
    await _context.SaveChangesAsync():
    return zone;
}
```
### **Devices:**
### `DELETE: api/Device/private/{id}`
#### **Description** Checks if a device exists before deleting it.
#### **Authentication:** Bearer Token with role of admin.
```C#
public async Task<ActionResult<Device>> AuthDeleteDevice(Guid id)
{
      var device = await _context.Device.FindAsync(id);
    if (device == null)
    {
          return NotFound();
    }

    _context.Device.Remove(device);
    await _context.SaveChangesAsync();

    return device;
}
```