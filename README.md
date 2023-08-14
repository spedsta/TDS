Working document for the TDS API


Example string input that will be part of the HMAC hash (this is in exact order):
AccessKey: this is the GUID that represents the client or organization ID. This is public and unique to each organization. Example: “649341d1-0250-480c-b221-8f6a456ac7e8”
Timestamp: 13-digit standard timestamp in string format ( the number of milliseconds elapsed since the epoch). Example: “1691351564000”
Nonce: the universally unique identifier (UUID) generated for each API request. Combined with the timestamp, the UUID ensures the uniqueness of API requests. 
HTTP Method: Capital letters for the HTTP method.  Example: “GET”, “POST”, “DELETE” etc.
The body of the request hashed by SHA256:  
The sending URL : Example: “'/v1.0/telegram1A”

The HMAC signature can be in the header as “sign”: “HMAC signature” OR in the URL as “mac=HMAC signature”.
