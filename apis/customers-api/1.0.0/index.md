---
# NOTICE: Copyright 2025 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "Customers API"
    version: "1.0.0"
    description: "No description"
  contract:
    mediaTypes:
    - "application/json"
    sections:
    - name: "Objects"
      elementOrder:
      - "#/contract/types/633555b3-9b35-429d-8b22-ee348f76af4f"
      - "#/contract/types/fe8f6d5a-274b-45b5-8827-a6bbb0bffc38"
      - "#/contract/types/dbf93efe-0e0c-48fc-adf6-824cf9cbe6ad"
    - name: "Operations"
      elementOrder:
      - "#/contract/resources/5827201e-c3a8-4889-a111-3a97604bcc0b"
      - "#/contract/resources/e57c34c2-be7d-4162-a703-697306688511"
    - name: "About"
      elementOrder:
      - "#/contract/texts/55bdcefe-2a44-4c1a-baf7-6377857a4829"
    resources:
      "5827201e-c3a8-4889-a111-3a97604bcc0b":
        path: "/customers"
        section: "#/contract/sections/42cfa68c-c438-4abf-be3f-8990aa7a725b"
        operations:
          cc7f761d-b8f8-4638-94f2-9c403013c2f9:
            name: "Get the list of customers"
            method: "GET"
            description: "Loads the list of customers"
            responses:
              c58423f8-fabc-420d-87aa-9d4bf19ce446:
                status: "200"
                description: "status 200"
                bodies:
                - type: "#/contract/types/fe8f6d5a-274b-45b5-8827-a6bbb0bffc38"
                  examples:
                  - value: "{\n\t\"Customer\": [{\n\t\t\t\"ID\": \"461140\",\n\t\t\t\"NAME\": \"Jason\",\n\t\t\t\"LAST_NAME\": \"HARRISON\",\n\t\t\t\"EMAIL\": \"jharrison5z@vistaprint.com\",\n\t\t\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\t\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\t\t\"COMPANY\": \"Zoonder\",\n\t\t\t\"CITY\": \"Portland\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"380630\",\n\t\t\t\"NAME\": \"VICTOR\",\n\t\t\t\"LAST_NAME\": \"COX\",\n\t\t\t\"EMAIL\": \"vcoxc9@virginia.edu\",\n\t\t\t\"JOB_TITLE\": \"Librarian\",\n\t\t\t\"CREDITCARDNUMBER\": \"30003746-83-0775\",\n\t\t\t\"COMPANY\": \"Skalith\",\n\t\t\t\"CITY\": \"Bend\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"149072\",\n\t\t\t\"NAME\": \"Beverly\",\n\t\t\t\"LAST_NAME\": \"WRIGHT\",\n\t\t\t\"EMAIL\": \"bwrighth3@arizona.edu\",\n\t\t\t\"JOB_TITLE\": \"Biostatistician\",\n\t\t\t\"CREDITCARDNUMBER\": \"6011204780-36-8180\",\n\t\t\t\"COMPANY\": \"Skynoodle\",\n\t\t\t\"CITY\": \"Indianapolis\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"678157\",\n\t\t\t\"NAME\": \"Kenneth\",\n\t\t\t\"LAST_NAME\": \"HARPER\",\n\t\t\t\"EMAIL\": \"kharperfu@craigslist.org\",\n\t\t\t\"JOB_TITLE\": \"Structural Engineer\",\n\t\t\t\"CREDITCARDNUMBER\": \"6249148211-57-8650\",\n\t\t\t\"COMPANY\": \"Dynava\",\n\t\t\t\"CITY\": \"Overland Park\",\n\t\t\t\"STATE\": \"\"\n\t\t}\t]\n}\n"
          ddd7ba1d-0237-44d5-af3e-9e70c3213cd5:
            name: "Create a customer"
            method: "POST"
            description: "adds a new customer"
            bodies:
            - type: "#/contract/types/633555b3-9b35-429d-8b22-ee348f76af4f"
              examples:
              - name: "application/json"
                value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            responses:
              "2f498f86-5966-4e28-9e0a-7b43b29e69eb":
                status: "201"
                description: "status 201"
                bodies:
                - type: "#/contract/types/633555b3-9b35-429d-8b22-ee348f76af4f"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
                  mediaTypes:
                  - "application/json"
              "56a7460e-238c-4f8f-8f6a-10d827b6ef7a":
                status: "409"
                description: "Status 409. Record could not be added"
                bodies:
                - type: "#/contract/types/dbf93efe-0e0c-48fc-adf6-824cf9cbe6ad"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"errorCode\": \"23000\",\n\t\"errorMessage\": \"Duplicate entry '461145' for key 'PRIMARY' - Line: 0\"\n}"
                  mediaTypes:
                  - "application/json"
      e57c34c2-be7d-4162-a703-697306688511:
        path: "/customers/{id}"
        section: "#/contract/sections/42cfa68c-c438-4abf-be3f-8990aa7a725b"
        pathVariables:
        - name: "id"
          type: "STRING"
          required: true
        operations:
          "9e712673-6c85-4b76-a32b-ff691d96f3e9":
            name: "Update a customer"
            method: "PUT"
            description: "Updates a customer"
            bodies:
            - type: "#/contract/types/633555b3-9b35-429d-8b22-ee348f76af4f"
              examples:
              - name: "application/json"
                value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            responses:
              fc5a60c3-ae43-401e-825f-1c4c953c2d09:
                status: "200"
                description: "Status 200"
                bodies:
                - type: "#/contract/types/633555b3-9b35-429d-8b22-ee348f76af4f"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
          dcc4d436-d070-44af-b639-a1efe7d96444:
            name: "Delete a customer"
            method: "DELETE"
            description: "Deletes a customer"
            responses:
              "0304316e-abc0-41cb-9b08-5d3c3001f347":
                status: "200"
                description: "Status 200"
    types:
      "633555b3-9b35-429d-8b22-ee348f76af4f":
        name: "Customer"
        type: "OBJECT"
        section: "#/contract/sections/2cd11c0e-b41c-4e5d-b532-11adc2c151d5"
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
      fe8f6d5a-274b-45b5-8827-a6bbb0bffc38:
        name: "Customers"
        type: "ARRAY"
        section: "#/contract/sections/2cd11c0e-b41c-4e5d-b532-11adc2c151d5"
        items:
          type: "#/contract/types/633555b3-9b35-429d-8b22-ee348f76af4f"
      dbf93efe-0e0c-48fc-adf6-824cf9cbe6ad:
        name: "Error"
        type: "OBJECT"
        section: "#/contract/sections/2cd11c0e-b41c-4e5d-b532-11adc2c151d5"
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
      "55bdcefe-2a44-4c1a-baf7-6377857a4829":
        title: "API built with Talend API Designer"
        content: "API designed with Talend API Designer. The Customers API implementation is built and is ready to deploy using Talend Cloud."
        section: "#/contract/sections/299e4e75-4dbd-49ee-ac49-e18c260d8ced"
  components: {}
api-tryin: |-
  {
    "version" : 6,
    "entities" : [ {
      "entity" : {
        "type" : "Project",
        "name" : "Customers API 1.0.0",
        "description" : "No description",
        "importedFrom" : "adaa8151-92f3-4c72-a743-41fe03796614"
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
            "id" : "cc7f761d-b8f8-4638-94f2-9c403013c2f9",
            "name" : "Get the list of customers",
            "description" : "Loads the list of customers",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/customers"
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
            "headersType" : "Form"
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "ddd7ba1d-0237-44d5-af3e-9e70c3213cd5",
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
            "id" : "9e712673-6c85-4b76-a32b-ff691d96f3e9",
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
            "id" : "dcc4d436-d070-44af-b639-a1efe7d96444",
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
      "name" : "Customers API 1.0.0",
      "importedFrom" : {
        "projectId" : "adaa8151-92f3-4c72-a743-41fe03796614"
      },
      "variables" : {
        "e9358f37-a1b7-49c7-85f6-4b5683a275e2" : {
          "name" : "BaseUrl",
          "value" : "https://example.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
