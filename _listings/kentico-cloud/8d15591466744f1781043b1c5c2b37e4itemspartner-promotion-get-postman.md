{
  "info": {
    "name": "Kentico Cloud Displaying the right content",
    "_postman_id": "311b862c-8f1d-4f92-9908-9522c983e956",
    "description": "Retrieve one personalization variant you want to display. To learn more about retrieving content, consult the [Delivery API reference](https://developer.kenticocloud.com/reference#delivery-api).\n\nSee <https://developer.kenticocloud.com/docs/personalizing-content#section-displaying-the-right-content> for more examples.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Displaying",
      "item": [
        {
          "id": "cfc13266-1b77-4ff7-9514-0b1856782664",
          "name": "8d15591466744f1781043b1c5c2b37e4ItemsPartnerPromotionGet",
          "request": {
            "url": "http://deliver.kenticocloud.com/8d155914-6674-4f17-8104-3b1c5c2b37e4/items/partner_promotion",
            "method": "GET",
            "header": [
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve one personalization variant you want to display. To learn more about retrieving content, consult the [Delivery API reference](https://developer.kenticocloud.com/reference#delivery-api).\n\nSee <https://developer.kenticocloud.com/docs/personalizing-content#section-displaying-the-right-content> for more examples."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e83c655e-ee74-4807-800b-3faff284eb60"
            }
          ]
        }
      ]
    }
  ]
}