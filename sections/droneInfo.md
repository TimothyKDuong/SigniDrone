# droneInfo

Find information on your drone via ID

## Endpoints

`GET` /droneInfo/{droneID}
finds information for a specific droneID

## Parameters
### Path Parameters
|Path parameter|Description|
|--|--|
| {droneID} |ID of drone to return   |

## Curl

```bash
curl -X 'GET' \
  ' https://signiant.com/signidroneapi/droneInfo?droneID=0001' \
  -H 'accept: application/json'
```

## Sample Request URL

    https://signiant.com/signidroneapi/droneInfo?droneID=0001

## Sample Response
```json
{
  "droneID": 0001,
  "droneName": "QuickerPickerUpper",
  "droneModel": "DroneDeck2.0",
  "droneStatus": 0
  "droneLocLat": 45.4215,
  "droneLocLon": 75.6972,
}
```

### Response definitions
|Query string parameter| Description |Data type |
|--|--|--|
| droneName | The given name of the drone. Set when the drone was created |string
| droneModel | The model of drone. | string
| droneStatus | The status of the drone. Set at 0 for offline and 1 for online|integer
| droneLocLat | Geographical coordinates of the drone's location (latitude) |integer
| droneLocLon |  Geographical coordinates of the drone's location (longitude)|integer
    
