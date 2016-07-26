# Google-Sheets-Functions
A repository of functions for google sheets

# Setup

## ImportJSON

Many of these functions require you to add the [`ImportJSON`](https://raw.githubusercontent.com/fastfedora/google-docs/master/scripts/ImportJSON/Code.gs) function in order to work. 

## Enable Advanced Services

Some of the functions require you to [enable the advanced services](https://developers.google.com/apps-script/guides/services/advanced).

# Contributing

Please fork and contribute!

## Geographic

### Elevation

Retrieve elevation data given lat/lon coordinates.

__Script__ 

```
function elevation(lat, lon) {
 url = "https://maps.googleapis.com/maps/api/elevation/json?locations=" + lat + "," + lon;
 result = ImportJSON(url, "/results/elevation"); 
 return(result[1])
}
```

## Science

### Fetch PubMed Formatted Citation - [Script](https://gist.github.com/danielecook/13a27f57ab5f1ff38dcd#file-pubmed-js)

Fetch a formatted citation from a pubmed identifier.

```
=pubmed(23149456) # Pubmed identifier
```

__The heritability of metabolic profiles in newborn twins.__<br />
Alul FY, Cook DE, Shchelochkov OA, Fleener LG, Berberich SL, Murray JC, Ryckman KK<br />
(2013 Mar) _Heredity_ 110 (3) 253-8

## Misc

### Url Shortener

```
function shortenUrl(longUrl) {
  var url = UrlShortener.Url.insert({
    longUrl: longUrl
  });
  return(url.id)
}
```




