## curl + jq

### Get routes + IDs
```
curl "http://ddot-beta.herokuapp.com/api/api/where/routes-for-agency/DDOT.json?key=BETA&format=json" | jq '.data.list | sort_by(.shortName) | .[] | {shortName, id}'
```

### Trips for routes at a specified time
```
curl "http://ddot-beta.herokuapp.com/api/api/where/trips-for-route/DDOT_5474.json?key=BETA&format=json&includeStatus=true&time=1392076790549" | jq '[.data.list[].status] | sort_by(.nextStop) | .[] | {nextStop, nextStopTimeOffset, predicted}'
```
