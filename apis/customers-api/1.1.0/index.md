---
# NOTICE: Copyright 2025 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "Customers API"
    version: "1.1.0"
    description: "An API for keeping track of your customers."
    license: {}
    contact: {}
  contract:
    mediaTypes:
    - "application/json"
    sections:
    - name: "Objects"
      elementOrder:
      - "#/contract/types/66169d4a-d37e-496d-a200-563c6ea71bb2"
      - "#/contract/types/c9ced7b9-71d9-4fdc-b57e-e4ebe18599d4"
      - "#/contract/types/57ce4f77-3e5f-4e2b-929c-fc66f0aa90c3"
    - name: "Operations"
      elementOrder:
      - "#/contract/resources/133d050e-1cef-4569-9d1e-c8e2a44dab12"
      - "#/contract/resources/a718aef6-d312-4396-a8c8-44616820a58f"
    - name: "About"
      elementOrder:
      - "#/contract/texts/db76b581-7aa0-481e-a610-df1dc0168d95"
    resources:
      "133d050e-1cef-4569-9d1e-c8e2a44dab12":
        path: "/customers"
        section: "#/contract/sections/f2e034fd-d9da-48bb-8d78-264895f4fbcf"
        operations:
          c23c4572-8375-4687-8267-81f9a0631b3d:
            name: "Get the list of customers"
            method: "GET"
            description: "Loads the list of customers"
            responses:
              "08133950-fd00-43c6-ad3f-46aaf787135d":
                status: "200"
                description: "status 200"
                bodies:
                - type: "#/contract/types/c9ced7b9-71d9-4fdc-b57e-e4ebe18599d4"
                  examples:
                  - value: "{\n\t\"Customer\": [{\n\t\t\t\"ID\": \"461140\",\n\t\t\t\"NAME\": \"Jason\",\n\t\t\t\"LAST_NAME\": \"HARRISON\",\n\t\t\t\"EMAIL\": \"jharrison5z@vistaprint.com\",\n\t\t\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\t\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\t\t\"COMPANY\": \"Zoonder\",\n\t\t\t\"CITY\": \"Portland\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"380630\",\n\t\t\t\"NAME\": \"VICTOR\",\n\t\t\t\"LAST_NAME\": \"COX\",\n\t\t\t\"EMAIL\": \"vcoxc9@virginia.edu\",\n\t\t\t\"JOB_TITLE\": \"Librarian\",\n\t\t\t\"CREDITCARDNUMBER\": \"30003746-83-0775\",\n\t\t\t\"COMPANY\": \"Skalith\",\n\t\t\t\"CITY\": \"Bend\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"149072\",\n\t\t\t\"NAME\": \"Beverly\",\n\t\t\t\"LAST_NAME\": \"WRIGHT\",\n\t\t\t\"EMAIL\": \"bwrighth3@arizona.edu\",\n\t\t\t\"JOB_TITLE\": \"Biostatistician\",\n\t\t\t\"CREDITCARDNUMBER\": \"6011204780-36-8180\",\n\t\t\t\"COMPANY\": \"Skynoodle\",\n\t\t\t\"CITY\": \"Indianapolis\",\n\t\t\t\"STATE\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"678157\",\n\t\t\t\"NAME\": \"Kenneth\",\n\t\t\t\"LAST_NAME\": \"HARPER\",\n\t\t\t\"EMAIL\": \"kharperfu@craigslist.org\",\n\t\t\t\"JOB_TITLE\": \"Structural Engineer\",\n\t\t\t\"CREDITCARDNUMBER\": \"6249148211-57-8650\",\n\t\t\t\"COMPANY\": \"Dynava\",\n\t\t\t\"CITY\": \"Overland Park\",\n\t\t\t\"STATE\": \"\"\n\t\t}\t]\n}\n"
          "06d754ee-5ff7-4109-b621-ba36dab0919f":
            name: "Create a customer"
            method: "POST"
            description: "Adds a new customer"
            bodies:
            - type: "#/contract/types/66169d4a-d37e-496d-a200-563c6ea71bb2"
              examples:
              - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            responses:
              "052ee9e7-1887-4d88-a028-9586d7e6f5f1":
                status: "201"
                description: "status 201"
                bodies:
                - type: "#/contract/types/66169d4a-d37e-496d-a200-563c6ea71bb2"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
              c9d5c096-ada2-4b41-854d-a3506e73ac62:
                status: "409"
                description: "Status 409. Record could not be added"
                bodies:
                - type: "#/contract/types/57ce4f77-3e5f-4e2b-929c-fc66f0aa90c3"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"errorCode\": \"23000\",\n\t\"errorMessage\": \"Duplicate entry '461145' for key 'PRIMARY' - Line: 0\"\n}"
      a718aef6-d312-4396-a8c8-44616820a58f:
        path: "/customers/{id}"
        section: "#/contract/sections/f2e034fd-d9da-48bb-8d78-264895f4fbcf"
        pathVariables:
        - name: "id"
          type: "STRING"
          required: true
        operations:
          "256fd533-55a8-42ea-9c69-2a62170f57b9":
            name: "Delete a customer"
            method: "DELETE"
            description: "Delete a customer"
            responses:
              "4231e513-e849-4dd3-b54f-c01ecc3df064":
                status: "200"
                description: "Status 200"
          "6f84c01b-7cab-4c59-9301-30c669a677dc":
            name: "Update a customer"
            method: "PUT"
            description: "Updates a customer."
            bodies:
            - type: "#/contract/types/66169d4a-d37e-496d-a200-563c6ea71bb2"
              examples:
              - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
            responses:
              "7592f440-808e-49a1-bbe0-ba5bca34e340":
                status: "200"
                description: "Status 200"
                bodies:
                - type: "#/contract/types/66169d4a-d37e-496d-a200-563c6ea71bb2"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"John\",\n\t\"LAST_NAME\": \"Smith\",\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\n\t\"JOB_TITLE\": \"Electrical Engineer\",\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\n\t\"COMPANY\": \"Zoonder\",\n\t\"CITY\": \"San Francisco\",\n\t\"STATE\": \"CA\"\n}"
    types:
      "66169d4a-d37e-496d-a200-563c6ea71bb2":
        name: "Customer"
        type: "OBJECT"
        section: "#/contract/sections/a655efde-940b-4adb-ad09-930775299fc7"
        required: false
        properties:
        - name: "ID"
          type: "STRING"
          required: false
        - name: "NAME"
          type: "STRING"
          required: false
        - name: "LAST_NAME"
          type: "STRING"
          required: false
        - name: "EMAIL"
          type: "STRING"
          required: false
        - name: "JOB_TITLE"
          type: "STRING"
          required: false
        - name: "CREDITCARDNUMBER"
          type: "STRING"
          required: false
        - name: "COMPANY"
          type: "STRING"
          required: false
        - name: "CITY"
          type: "STRING"
          required: false
        - name: "STATE"
          type: "STRING"
          required: false
        examples:
        - value: "{\r\n\t\"ID\": \"461145\",\r\n\t\"NAME\": \"John\",\r\n\t\"LAST_NAME\": \"Smith\",\r\n\t\"EMAIL\": \"jsmith@vistaprint.com\",\r\n\t\"JOB_TITLE\": \"Electrical Engineer\",\r\n\t\"CREDITCARDNUMBER\": \"4343354898-76-9480\",\r\n\t\"COMPANY\": \"Zoonder\",\r\n\t\"CITY\": \"San Francisco\",\r\n\t\"STATE\": \"CA\"\r\n}"
      c9ced7b9-71d9-4fdc-b57e-e4ebe18599d4:
        name: "Customers"
        type: "ARRAY"
        section: "#/contract/sections/a655efde-940b-4adb-ad09-930775299fc7"
        items:
          type: "#/contract/types/66169d4a-d37e-496d-a200-563c6ea71bb2"
          required: false
      "57ce4f77-3e5f-4e2b-929c-fc66f0aa90c3":
        name: "Error"
        type: "OBJECT"
        section: "#/contract/sections/a655efde-940b-4adb-ad09-930775299fc7"
        properties:
        - name: "ID"
          type: "STRING"
          required: true
        - name: "errorCode"
          type: "INTEGER"
          required: false
          minimum: 400
          maximum: 599
        - name: "errorMessage"
          type: "STRING"
          required: false
    texts:
      db76b581-7aa0-481e-a610-df1dc0168d95:
        title: "API built with Talend API Designer"
        content: "API designed with Talend API Designer. The Customers API implementation is built and is ready to deploy using Talend Cloud."
        section: "#/contract/sections/183e5fcd-9a0d-4899-a6c0-0e7f665ce650"
  components: {}
api-tryin: |-
  {
    "version" : 6,
    "entities" : [ {
      "entity" : {
        "type" : "Project",
        "name" : "Customers API 1.1.0",
        "description" : "An API for keeping track of your customers.",
        "importedFrom" : "68d10d7d-624c-4102-9437-294743aa6384"
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
            "id" : "c23c4572-8375-4687-8267-81f9a0631b3d",
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
            "id" : "06d754ee-5ff7-4109-b621-ba36dab0919f",
            "name" : "Create a customer",
            "description" : "Adds a new customer",
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
            "id" : "256fd533-55a8-42ea-9c69-2a62170f57b9",
            "name" : "Delete a customer",
            "description" : "Delete a customer",
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
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "6f84c01b-7cab-4c59-9301-30c669a677dc",
            "name" : "Update a customer",
            "description" : "Updates a customer.",
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
        } ]
      }, {
        "entity" : {
          "type" : "Service",
          "name" : "About"
        }
      } ]
    } ],
    "environments" : [ {
      "name" : "Customers API 1.1.0",
      "importedFrom" : {
        "projectId" : "68d10d7d-624c-4102-9437-294743aa6384"
      },
      "variables" : {
        "f08b6f6d-4ebd-4f88-ae39-98a4ba3d781c" : {
          "name" : "BaseUrl",
          "value" : "https://example.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
