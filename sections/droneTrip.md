# droneTrip

Gives information about your drone's recent trips

## Endpoints

`GET` /droneTrip/{droneID}?
finds range of travel information for a specific droneID

## Parameters
### Path Parameters
|Path parameter|Description|
|--|--|
| {droneID} |ID of drone to return   |

### Query string parameters
|Path parameter|Description|
|--|--|
|tripDate| The day of the trip(s) to include in the response. Will report the current day's trips if not included. Submitted in YYYYMMDD format. |
|tripNo| The number of trips to include in the response. Default is 4 |

## Curl

```bash
curl -X 'GET' \
  ' https://signiant.com/signidroneapi/droneTrip?droneID=0001&tripDate=20220101&tripNo=2' \
  -H 'accept: application/json'
```

## Sample Request URL

    https://signiant.com/signidroneapi/droneRange?droneID=0001&tripDate=20220101&tripNo=2

## Sample Response
```json
{
  "droneTrip":[
	  {
		  "droneID":0001,
		  20220101:{
			  "tripCount":01 {
				  "tripStartTime" : 1659097012012,
				  "tripEndTime" : 1659104312219,
				  "tripDuration" : 7300207
				  "tripType" : "fliming"
				  }
				 "tripCount":02 {
				 "tripStartTime" : 1659127012012,
				  "tripEndTime" : 1659129312219,
				  "tripDuration" : 2300207
				  "tripType" : "delivery"
				  }
			  }
		}
	]	  
}
```

### Response definitions
|Query string parameter| Description |Data type |
|--|--|--|
| droneID | The drone you selected based on ID. |integer
| {tripDate} | Date of the trip, presented in YYYYMMDD | integer
| tripStartTime | The time that the trip started, calculated at the moment the drone lifts off. Unix format (ms since 1970) in ETC |integer
| tripEndTime | The time that the trip ended, calculated at the moment the drone lands. Unix format (ms since 1970) in ETC |integer
|tripDuration | The total duration of the trip, measured in millisecionds | integer
| tripType |  The type of trip the drone was one, as chosen by the user. The currently available types of trips are "filming", "delivery", "sport", and other|string`
    
