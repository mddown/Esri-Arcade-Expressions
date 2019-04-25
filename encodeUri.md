## Encode uri string
### Helpful when building parameterized uri's
### This does not cover all character encodings...

- input string = LGA Terminal B
- output string = LGA%20Terminal%20B

```javascript
function Permalink(string){
    var space = Replace(string, ' ', '%20')
    var hyphon = Replace(space, '-', '%2D')
    var apos = Replace(hyphon, "'", '%27')
    var and = Replace(apos, '&', '%26')
    var comma = Replace(and, ',', '%2C')
    var baseUrl = "https://panynj.maps.arcgis.com/apps/webappviewer/index.html?id=d5b75282cc4343399de25fcfd3468f48&query=OutdoorPOI_LGA_Public_View_2617%2CPOI_Name%2C"
    
    var fullUrl = "'"+baseUrl + comma + "'"
    fullUrl
}

var permalink = Permalink($feature.POI_Name)
return Text(permalink)
