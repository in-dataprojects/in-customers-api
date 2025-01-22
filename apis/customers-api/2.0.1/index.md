---
# NOTICE: Copyright 2025 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "Customers API"
    version: "2.0.1"
    description: "No description"
  contract:
    mediaTypes:
    - "application/json"
    sections:
    - name: "Objects"
      elementOrder:
      - "#/contract/types/b0d8fd21-84f6-4bdb-97a0-90863cbe5321"
      - "#/contract/types/b18bcf10-16f4-4551-b0d5-fab2fa3ebcb3"
      - "#/contract/types/fc497773-0352-494c-b8ae-544665b51a39"
    - name: "Operations"
      elementOrder:
      - "#/contract/resources/80945456-f058-4675-9d4e-d2a6a5810bd1"
      - "#/contract/resources/0ce6a4cf-375d-420f-ba6a-3f26a09290de"
    - name: "About"
      elementOrder:
      - "#/contract/texts/baa1d8c8-342c-4661-a547-5309326e5002"
    resources:
      "80945456-f058-4675-9d4e-d2a6a5810bd1":
        path: "/customers"
        section: "#/contract/sections/fc011e8f-64b7-403c-b992-9116d950fb74"
        operations:
          "0be53fba-10ff-4b3a-8b42-8f5bebf521fd":
            name: "Get the list of customers"
            method: "GET"
            description: "Loads the list of customers"
            queryParameters:
            - name: "start"
              type: "INTEGER"
              description: "Start position for a group of customers to get"
              required: true
            - name: "pageSize"
              type: "INTEGER"
              description: "Number of customers in the group to get"
              required: true
            responses:
              "525c16c7-2201-41c6-ac47-8f372688fe04":
                status: "200"
                description: "status 200"
                bodies:
                - type: "#/contract/types/b18bcf10-16f4-4551-b0d5-fab2fa3ebcb3"
                  examples:
                  - value: "{\n\t\"Customer\": [{\n\t\t\t\"ID\": \"461140\",\n\t\t\t\"NAME\": \"Jason\",\n\t\t\t\"LAST_NAME\": \"HARRISON\",\n\t\t\t\"EMAIL\": \"jharrison5z@vistaprint.com\",\n\t\t\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\t\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\t\t\"COMPANY\": \"Zoonder\",\n\t\t\t\"CITY\": \"Portland\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"380630\",\n\t\t\t\"NAME\": \"VICTOR\",\n\t\t\t\"LAST_NAME\": \"COX\",\n\t\t\t\"EMAIL\": \"vcoxc9@virginia.edu\",\n\t\t\t\"JOB_TITLE\": \"Librarian\",\n\t\t\t\"CREDITCARDNUMBER\": \"30003746-83-0775\",\n\t\t\t\"COMPANY\": \"Skalith\",\n\t\t\t\"CITY\": \"Bend\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"149072\",\n\t\t\t\"NAME\": \"Beverly\",\n\t\t\t\"LAST_NAME\": \"WRIGHT\",\n\t\t\t\"EMAIL\": \"bwrighth3@arizona.edu\",\n\t\t\t\"JOB_TITLE\": \"Biostatistician\",\n\t\t\t\"CREDITCARDNUMBER\": \"6011204780-36-8180\",\n\t\t\t\"COMPANY\": \"Skynoodle\",\n\t\t\t\"CITY\": \"Indianapolis\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"678157\",\n\t\t\t\"NAME\": \"Kenneth\",\n\t\t\t\"LAST_NAME\": \"HARPER\",\n\t\t\t\"EMAIL\": \"kharperfu@craigslist.org\",\n\t\t\t\"JOB_TITLE\": \"Structural Engineer\",\n\t\t\t\"CREDITCARDNUMBER\": \"6249148211-57-8650\",\n\t\t\t\"COMPANY\": \"Dynava\",\n\t\t\t\"CITY\": \"Overland Park\",\n\t\t\t\"STATE\": \"\"\n\t\t}\t]\n}\n"
          "4fd21636-2361-43f1-97d1-ccad80afcc79":
            name: "Create a customer"
            method: "POST"
            description: "adds a new customer"
            bodies:
            - type: "#/contract/types/b0d8fd21-84f6-4bdb-97a0-90863cbe5321"
              examples:
              - name: "application/json"
                value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            responses:
              "29c707f3-1d87-4b51-9a3f-3b16b499a05f":
                status: "201"
                description: "status 201"
                bodies:
                - type: "#/contract/types/b0d8fd21-84f6-4bdb-97a0-90863cbe5321"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
                  mediaTypes:
                  - "application/json"
              d5066923-2cb8-45fe-aec5-b2e28c8778aa:
                status: "409"
                description: "Status 409. Record could not be added"
                bodies:
                - type: "#/contract/types/fc497773-0352-494c-b8ae-544665b51a39"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"errorCode\": \"23000\",\n\t\"errorMessage\": \"Duplicate entry '461145' for key 'PRIMARY' - Line: 0\"\n}"
                  mediaTypes:
                  - "application/json"
      "0ce6a4cf-375d-420f-ba6a-3f26a09290de":
        path: "/customers/{id}"
        section: "#/contract/sections/fc011e8f-64b7-403c-b992-9116d950fb74"
        pathVariables:
        - name: "id"
          type: "STRING"
          required: true
        operations:
          "2c51fc4a-9cd7-4ef7-9ee2-d434c9294fda":
            name: "Update a customer"
            method: "PUT"
            description: "Updates a customer"
            bodies:
            - type: "#/contract/types/b0d8fd21-84f6-4bdb-97a0-90863cbe5321"
              examples:
              - name: "application/json"
                value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            responses:
              d8a42838-c13e-4072-9983-0c796aa16f60:
                status: "200"
                description: "Status 200"
                bodies:
                - type: "#/contract/types/b0d8fd21-84f6-4bdb-97a0-90863cbe5321"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
          "3b17eca9-f3ef-4e06-8c10-7d074361e970":
            name: "Delete a customer"
            method: "DELETE"
            description: "Deletes a customer"
            responses:
              d351c079-c278-47ad-9b68-38b06db32e42:
                status: "200"
                description: "Status 200"
    types:
      b0d8fd21-84f6-4bdb-97a0-90863cbe5321:
        name: "Customer"
        type: "OBJECT"
        section: "#/contract/sections/b87f8574-a74d-498e-ae80-0088a26db3be"
        properties:
        - name: "ID"
          type: "STRING"
        - name: "NAME"
          type: "STRING"
        - name: "LAST_NAME"
          type: "STRING"
        - name: "EMAIL"
          type: "STRING"
        - name: "JOB_TITLE"
          type: "STRING"
        - name: "CREDITCARDNUMBER"
          type: "STRING"
        - name: "COMPANY"
          type: "STRING"
        - name: "CITY"
          type: "STRING"
        - name: "STATE"
          type: "STRING"
        examples:
        - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
      b18bcf10-16f4-4551-b0d5-fab2fa3ebcb3:
        name: "Customers"
        type: "ARRAY"
        section: "#/contract/sections/b87f8574-a74d-498e-ae80-0088a26db3be"
        items:
          type: "#/contract/types/b0d8fd21-84f6-4bdb-97a0-90863cbe5321"
      fc497773-0352-494c-b8ae-544665b51a39:
        name: "Error"
        type: "OBJECT"
        section: "#/contract/sections/b87f8574-a74d-498e-ae80-0088a26db3be"
        properties:
        - name: "ID"
          type: "STRING"
          required: true
        - name: "errorCode"
          type: "INTEGER"
          minimum: 400
          maximum: 599
        - name: "errorMessage"
          type: "STRING"
    texts:
      baa1d8c8-342c-4661-a547-5309326e5002:
        title: "API built with Talend API Designer"
        content: "API designed with Talend API Designer. The Customers API implementation is built and is ready to deploy using Talend Cloud."
        section: "#/contract/sections/bab739be-bed5-4cf7-b17a-8de9cf10669b"
  components: {}
api-tryin: |-
  {
    "version" : 6,
    "entities" : [ {
      "entity" : {
        "type" : "Project",
        "name" : "Customers API 2.0.1",
        "description" : "No description",
        "importedFrom" : "85c548fd-562e-4871-bd1f-c606fd92a4d3"
      },
      "children" : [ {
        "entity" : {
          "type" : "Service",
          "name" : "Objects"
        }
      }, {
        "entity" : {
          "type" : "Service",
          "name" : "Operations"
        },
        "children" : [ {
          "entity" : {
            "type" : "Request",
            "id" : "0be53fba-10ff-4b3a-8b42-8f5bebf521fd",
            "name" : "Get the list of customers",
            "description" : "Loads the list of customers",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/customers",
              "query" : {
                "delimiter" : "&",
                "items" : [ {
                  "name" : "start",
                  "value" : "",
                  "enabled" : true
                }, {
                  "name" : "pageSize",
                  "value" : "",
                  "enabled" : true
                } ]
              }
            },
            "method" : {
              "link" : "",
              "name" : "GET"
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Accept",
              "value" : "application/json"
            } ],
            "headersType" : "Form",
            "uriEditor" : true
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "4fd21636-2361-43f1-97d1-ccad80afcc79",
            "name" : "Create a customer",
            "description" : "adds a new customer",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/customers"
            },
            "method" : {
              "link" : "",
              "name" : "POST",
              "requestBody" : true
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Content-Type",
              "value" : "application/json"
            }, {
              "enabled" : true,
              "name" : "Accept",
              "value" : "application/json"
            } ],
            "headersType" : "Form",
            "body" : {
              "bodyType" : "Text",
              "textBody" : "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            }
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "2c51fc4a-9cd7-4ef7-9ee2-d434c9294fda",
            "name" : "Update a customer",
            "description" : "Updates a customer",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/customers/{id}"
            },
            "method" : {
              "link" : "",
              "name" : "PUT",
              "requestBody" : true
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Content-Type",
              "value" : "application/json"
            }, {
              "enabled" : true,
              "name" : "Accept",
              "value" : "application/json"
            } ],
            "headersType" : "Form",
            "body" : {
              "bodyType" : "Text",
              "textBody" : "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            }
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "3b17eca9-f3ef-4e06-8c10-7d074361e970",
            "name" : "Delete a customer",
            "description" : "Deletes a customer",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/customers/{id}"
            },
            "method" : {
              "link" : "",
              "name" : "DELETE"
            },
            "headers" : [ ],
            "headersType" : "Form"
          }
        } ]
      }, {
        "entity" : {
          "type" : "Service",
          "name" : "About"
        }
      } ]
    } ],
    "environments" : [ {
      "name" : "Customers API 2.0.1",
      "importedFrom" : {
        "projectId" : "85c548fd-562e-4871-bd1f-c606fd92a4d3"
      },
      "variables" : {
        "eb3b7770-cc15-4b62-8b92-da55a65bf55a" : {
          "name" : "BaseUrl",
          "value" : "https://example.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
