# Postman API Inspection Notes

### OVERVIEW
#### There are 4 main flows I have inspected:

 1. Visitor accesses the profile page
 2. Visitor exchanges their information with the visited profile
 3. Visitor downloads the profile contact without sharing information
 4. Visitor downloads the profile contact, then share their contacts with the visited profile user

#### The main steps to check those four flows starts with:

 1. Use browser DevTools to identify main API requests
 2. Go to the Network tab, select the **XHR** filter (to focus on API requests)
 3. Perform the needed actions for the defined flows to identify called APIs for each flow
 4. Look for API requests related to each flow's actions
> In each flow, I mainly focus on the APIs that get or save information
 5. Inspect the request's details
 6. Use Postman to simulate the requests

###  DETAIL OF INSPECTION

#### 1) Scope of the inspection
- Request headers
- Response headers
- Request payloads (where applicable)
- Response payloads

#### 2) Test Environment
- **Testing Environment**: Production
- **Operating System**: macOS Sonoma 14
- **Browser**: Safari(v17.4.1), Chrome (v134.0.6998.166)
- **Testing tool**: Postman (v11.39.0), DevTools 134

#### 3) Authentication

There is no authentication needed in with these flows as a visitor

#### 4) Testing Approach
- **Funtional testing**: Verify endpoints perform as expected
- **Header validation**: Verify request/response headers for correct values and formats
- **Payload validation**: Verify request/response payloads for correct structure, data types and values
- **Error handing testing**: Verify the API responds appropriately to invalid requests

**Base URL:** https://api.linqapp.com



|                        Endpoint                        | HTTP Method | Headers          |                                     Request Payload                                     |  Response |                                Comment                                |   |
|:------------------------------------------------------:|:-----------:|------------------|:---------------------------------------------------------------------------------------:|:---------:|:---------------------------------------------------------------------:|---|
| /api/v2/contacts/{id}                                  | GET         | application/json | None                                                                                    | Code: 200 | Return profile contact information                                    |   |
| /api/v3/contact_exchange_settings/{id}/                | GET         | application/json | None                                                                                    | Code: 200 | Return profile exchange information                                   |   |
| /api/v2/cards/{card_connecting_code}/contact_downloads | POST        | application/json | {   "email": "xtntest75@gmail.com",   "name": "Keo",   "phone_number": "+14342828008" } | Code: 200 | Visitor registers to download profile contact via phone or/and number |   |
| /api/v2/user_contacts                                  | POST        | application/json | {   "contact_id": 2242318,   "user_id": 562487,   "created_from_card_id": 634101 }      | Code: 200 | Create contact information for visitor                                |   |
| /api/v1/cards/{card_connecting_code}/download_contact  | GET         | text/vcard       | None                                                                                    | Code: 200 | Download profile contact information as card                          |   |
| /{card_connecting_code}?r=link                         | GET         | text/html        | None                                                                                    | Code: 200 | Get the profile information when a visitor accesses a profile         |   |

	    
# NOTES, QUESTIONS & CONCERN
>  Question: Why does the application need to call the "Exchange Contact Info" API when the user hasn't clicked the "Exchange Contact" button yet?



