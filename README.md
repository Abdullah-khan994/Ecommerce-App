{
	"info": {
		"_postman_id": "5b0609b9-bdbd-42f2-964d-8c048c7dae18",
		"name": "eCommerce App",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
	},
	"item": [
		{
			"name": "Get Categories",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/listCategory",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"listCategory"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get Shipping Areas",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/listShipping?q=was",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"listShipping"
					],
					"query": [
						{
							"key": "q",
							"value": "was"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Get Product Details",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/getProductDetails?id=3",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"getProductDetails"
					],
					"query": [
						{
							"key": "id",
							"value": "3"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Get Products",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/listProduct?category_id=4",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"listProduct"
					],
					"query": [
						{
							"key": "page",
							"value": "1",
							"disabled": true
						},
						{
							"key": "count",
							"value": "5",
							"disabled": true
						},
						{
							"key": "q",
							"value": null,
							"disabled": true
						},
						{
							"key": "col",
							"value": null,
							"disabled": true
						},
						{
							"key": "ord",
							"value": null,
							"disabled": true
						},
						{
							"key": "category_id",
							"value": "4"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Get News",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/listNews",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"listNews"
					],
					"query": [
						{
							"key": "page",
							"value": "1",
							"disabled": true
						},
						{
							"key": "count",
							"value": "1",
							"disabled": true
						},
						{
							"key": "q",
							"value": "dapibus",
							"disabled": true
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Get News Details",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/getNewsDetails?id=10",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"getNewsDetails"
					],
					"query": [
						{
							"key": "id",
							"value": "10"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Get Featured News Copy",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/listFeaturedNews",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"listFeaturedNews"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get Info",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{BASE_URL}}/services/listCategory",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"services",
						"listCategory"
					]
				}
			},
			"response": []
		},
		{
			"name": "Save Firebsae Token",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Security",
						"value": "secure_code",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n        \"device\": \"sadasd\",\n        \"os_version\": \"1\",\n        \"app_version\": \"1\",\n        \"serial\": \"sad\",\n        \"regid\": \"sadasd\"\n    }",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/insertOneFcm",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"insertOneFcm"
					]
				}
			},
			"response": []
		},
		{
			"name": "Post Order",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Security",
						"value": "secure_code",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n  \"product_order\" : {\n  \"buyer\" : \"Mian Asad Ali\",\n  \"address\" : \"Some address\",\n  \"email\" : \"mianasadali@gmail.com\",\n  \"shipping\" : \"Economy\",\n  \"shipping_rate\" : \"20\",\n  \"shipping_location\" : \"Washington, US\",\n  \"date_ship\" : 1645144704466,\n  \"phone\" : \"123456\",\n  \"comment\" : \"some comment\",\n  \"status\" : \"\",\n  \"total_fees\" : 123,\n  \"tax\" : 2,\n  \"serial\" : \"123456\",\n  \"created_at\" : 1645144704466,\n  \"updated_at\" : 1645144704466\n  },\n  \"product_order_detail\" : [\n    {\n     \"product_id\" : 3,\n     \"product_name\" : \"Mian Asad Ali\",\n     \"amount\" : 24,\n     \"price_item\" : 40,\n     \"created_at\" : 1645144704466,\n     \"updated_at\" : 1645144704466\n    }\n    ]\n  \n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{BASE_URL}}/{{API_BASE}}/submitProductOrder",
					"host": [
						"{{BASE_URL}}"
					],
					"path": [
						"{{API_BASE}}",
						"submitProductOrder"
					]
				}
			},
			"response": []
		}
	],
	"event": [
		{
			"listen": "prerequest",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		},
		{
			"listen": "test",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		}
	],
	"variable": [
		{
			"key": "BASE_URL",
			"value": "https://tutorials.mianasad.com/ecommerce",
			"type": "string"
		},
		{
			"key": "API_BASE",
			"value": "services",
			"type": "string"
		}
	]
}
