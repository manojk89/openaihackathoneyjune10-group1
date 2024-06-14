# openaihackathoneyjune10-group1

**Problem Statement**

In the rapidly growing travel and tourism industry, travelers are faced with an overwhelming number of hotel options. Choosing the right hotel can significantly impact their travel experience. With the advent of big data and advanced analytics, there is an opportunity to leverage various data sources to provide personalized hotel recommendations that match individual preferences and needs.

**Collecting Data:**

We collected open data from https://www.cs.cmu.edu/~jiweil/html/hotel-review.html which has 1000 hotel information and 8lakhs user reviews on the hotel. we transformed the data into combined objects of reviews and hotel data which has following stucture:

```json
{
  "_id": {
    "$oid": "666be4e911abad68f7af88aa"
  },
  "ratings": {
    "service": 5,
    "cleanliness": 5,
    "overall": 5,
    "value": 5,
    "location": 5,
    "sleep_quality": 5,
    "rooms": 5
  },
  "title": "“Truly is \"Jewel of the Upper Wets Side\"”",
  "text": "Stayed in a king suite for 11 nights and yes it cots us a bit but we were happy with the standard of room, the location and the friendliness of the staff. Our room was on the 20th floor overlooking Broadway and the madhouse of the Fairway Market. Room was quite with no noise evident from the hallway or adjoining rooms. It was great to be able to open windows when we craved fresh rather than heated air. The beds, including the fold out sofa bed, were comfortable and the rooms were cleaned well. Wi-fi access worked like a dream with only one connectivity issue on our first night and this was promptly responded to with a call from the service provider to ensure that all was well. The location close to the 72nd Street subway station is great and the complimentary umbrellas on the drizzly days were greatly appreciated. It is fabulous to have the kitchen with cooking facilities and the access to a whole range of fresh foods directly across the road at Fairway.\nThis is the second time that members of the party have stayed at the Beacon and it will certainly be our hotel of choice for future visits.",
  "author": {
    "username": "Papa_Panda",
    "num_cities": 22,
    "num_helpful_votes": 12,
    "num_reviews": 29,
    "num_type_reviews": 24,
    "id": "8C0B42FF3C0FA366A21CFD785302A032",
    "location": "Gold Coast"
  },
  "date_stayed": "December 2012",
  "offering_id": 93338,
  "num_helpful_votes": 0,
  "date": "December 17, 2012",
  "id": 147643103,
  "via_mobile": false,
  "hoteldata": {
    "hotel_class": 3,
    "region_id": 60763,
    "url": "http://www.tripadvisor.com/Hotel_Review-g60763-d93338-Reviews-Hotel_Beacon-New_York_City_New_York.html",
    "phone": "",
    "details": null,
    "address": {
      "region": "NY",
      "street-address": "2130 Broadway at 75th Street",
      "postal-code": "10023",
      "locality": "New York City"
    },
    "type": "hotel",
    "id": 93338,
    "name": "Hotel Beacon"
  }
}
```

We have converted huge data set into 800+ different files each containing 1000 reviews. so that the data is easy to index during RAG.

**Building RAG with your own Data**

We have used azure open ai playground to deploy gpt 3.5 turbo model and datasource with upload options into the storage account. We have give the system a message of "You are an AI assistant that helps people find information on hotels based on datasource provided"

<img width="1783" alt="image" src="https://github.com/manojk89/openaihackathoneyjune10-group1/assets/172774224/94f2586c-b702-4816-abc1-dbb5bbb86578">

**Deploying the Model and Consuming in client application**

We used webapp deploy option available in playground with B1 tier, which was then deployed to https://group1hotelsuggestions.azurewebsites.net/

**Examples:**

We have tried following examples and system started responding with right results with citation.


1.suggest me good hotels in seattle with great location and neatness with lot of restaurant options near by
2.get me reviews of user named Refined-Bohemian
3.get me the top user which has highest reviews
4.get me reviews of that user
5.best hotel for honeymoon in new york
6.suggest me good hotels in seattle with great location and neatness with 7.lot of restaurant options near by
8.give me the user who has highest liked reviews
9.get all reviews of the user
10.suggest me good hotel for honeymoon in seattle
11.best hotel in bangalore

<img width="1792" alt="image" src="https://github.com/manojk89/openaihackathoneyjune10-group1/assets/172774224/76da3e9e-2881-4f43-8f87-ff64bb49b846">
<img width="1790" alt="image" src="https://github.com/manojk89/openaihackathoneyjune10-group1/assets/172774224/ba98e9bc-b439-4419-909a-3b2303bc9bf4">
<img width="1792" alt="image" src="https://github.com/manojk89/openaihackathoneyjune10-group1/assets/172774224/eabaa8ca-f443-4352-9d5c-0583f90c6096">







