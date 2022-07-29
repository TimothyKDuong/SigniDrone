# droneChange

Updates a drone with form data

## Endpoints

`PUT` /droneChange/{droneID}?
changes information for a specific droneID

## Parameters
### Path Parameters
|Path parameter|Description|
|--|--|
| {droneID} |ID of drone to return   |

### Query Parameters
|Query string parameter| Required/optional| Description |Data type |
|--|--|--|--|
| userID |Optional | User the drone is to be assigned to | string
| droneName | Optional | Name the drone is to be changed to |string


## Sample Curl

```bash
curl -X 'PUT' \
  ' https://signiant.com/signidroneapi/droneChange?droneID=0001+droneName="DrondaCivic"' \
  -H 'accept: application/json'
```

## Sample Request URL

    https://signiant.com/signidroneapi/droneInfo?droneID=0001+droneName="DrondaCivic"

## Sample Response
```json
{ "code": 200
  "message": "successful operation",
}
```    

### Example Value
```json
{
  "droneID": 0001,
  "userName": Sig Niant
  "userID": 199714911420
  "droneName": "DrondaCivic",
  "droneModel": "DroneDeck2.0",
  "droneOnline": "true"
  "droneLocLat": 45.4215,
  "droneLocLon": 75.6972,
}
```

See also: [droneInfo](https://github.com/TimothyKDuong/SigniDroneAPI/edit/main/sections/droneInfo.md)

### Responses 
|Response Item| Description| 
|--|--|
| 200 |Successful operation
| 400 | Invalid inputs supplied
| 404 | DroneID not found |
