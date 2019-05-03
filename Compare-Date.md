## Compare Date
### check if today is less/greater than dates in attributes

```javascript
var open = $feature.StartDate
var closed = $feature.EndDate
var present = Today()

IF(present >= open && present <= closed){ 
	return 'Active'
} else {  
	return 'Inactive'
}
