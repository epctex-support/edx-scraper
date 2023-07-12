[https://apify.com/epctex/edx-scraper](https://apify.com/epctex/edx-scraper?fpr=yhdrb)

# Actor - edx Scraper

## edx scraper

Since edx doesn't provide a proper free API, this actor should help you to retrieve data from it.

The edx data scraper supports the following features:

- Scrape any courses you would like to get - You can search for a specific keyword and scrape the results accordingly.

- Apply any of the filters - You can apply any filter provided by the website.

- Scrape by language - You can filter by language from the actor default.

- Limit the results by page or amount of property. - If you don't want to get all the results but a specific amount you can limit it.

## Bugs, fixes, updates, and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/edx-scraper/issues).

## Input Parameters

The input of this scraper should be JSON containing the list of pages on edx that should be visited. Possible fields are:

- `search`: (Optional) (String) Search keyword that you would like to search the courses in.

- `language`: (Optional) (String) Scrape the results by the course language.

- `maxItems`: (Optional) (Number) You can limit scraped items. This should be useful when you search through the big lists or search results.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use <a href="https://www.apify.com/docs/proxy">Apify Proxy</a>.

### Compute Unit Consumption

The actor is optimized to run blazing fast and scrape many listings as possible. Therefore, it forefronts all listing detail requests. If the actor doesn't block very often it'll scrape 100 listings in 1 minute with ~0.03-0.04 compute units.

### edx Scraper Input example

```json
{
  "search":"span",
  "language":"English",
  "maxItems":10,
  "proxy":{
    "useApifyProxy":true
  }
}

```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with a failure state and output an explanation of what is wrong.

## edx Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any language (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this edx actor.

## Scraped edx Properties

The structure of each item in edx listings looks like this:

###Course Output

```json
{
    "uuid": "09222e6c-a1bc-4307-ba80-294ea4281117",
    "title": "Shaping Work of the Future",
    "inProspectus": true,
    "prospectusPath": "/course/shaping-work-of-the-future",
    "organizationShortCodeOverride": "",
    "organizationLogoOverrideUrl": null,
    "courseType": "verified-audit",
    "inYearValue": null,
    "activeCourseRun": {
        "key": "course-v1:MITx+15.662x+1T2020",
        "type": "verified",
        "marketingUrl": "https://www.edx.org/course/shaping-work-of-the-future-3",
        "minEffort": 4,
        "maxEffort": 5,
        "weeksToComplete": 8
    },
    "image": {
        "src": "https://prod-discovery.edx-cdn.org/media/course/image/09222e6c-a1bc-4307-ba80-294ea4281117-e28e19d05647.small.jpg"
    },
    "locationRestriction": null,
    "owners": [
        {
            "key": "MITx",
            "logoImageUrl": "https://prod-discovery.edx-cdn.org/organization/logos/2a73d2ce-c34a-4e08-8223-83bca9d2f01d-2cc8854c6fee.png",
            "name": "Massachusetts Institute of Technology"
        }
    ],
    "recentEnrollmentCount": 1149,
    "topics": [],
    "additionalMetadata": null,
    "objectID": "course-09222e6c-a1bc-4307-ba80-294ea4281117",
    "cardType": "course",
    "cardIndex": 3,
    "url": "https://learning.edx.org/course/course-v1:MITx+15.662x+1T2020/home."
}
```

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that are available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
