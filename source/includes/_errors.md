# Response & Error Codes

The RFDS API uses http error codes to indicate the success of the failure of the requests.


Error Code | Meaning
---------- | -------
200 | Success -- The attempted action was a success. For example, if it was a DELETE, then this code confirms the resource has been correctly deleted.
400 | Bad Request -- Bad request.
401 | Unauthorized -- Invalid API key.
403 | Forbidden -- You lack permission to access the requested resource.
404 | Not Found -- The specified resource could not be found.
405 | Method Not Allowed
410 | Gone
422 | The request was invalid. Most probably the number of parameters or the values of the parameters was invalid. The same request shouldn't be attempted again.
500 | Internal Server Error -- Probably let the developers know of this.
503 | Service Unavailable
