# CRUD


## Status Codes Based On REST Methods











- Q. In your own words, describe what each group of status code represents:

100’s = Informational status codes; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.
200’s = Success codes that let the client know that the request was accepted 
300’s = Redirection codes. They tell the client that the resource that they're trying to get is not at that current location anymore
400’s = error codes. These are invalid requests to a server . There are several causes to this, timeouts, wrong URI, missing authentication, etc. A client is sending incorrect input and should confirm the input parameters are correct before retrying the request.


500’s = server error codes. They often indicate problems with an overwhelmed server or unreachable servers


- Q. What is a status code 202?

- A. Request was accepted 


- Q. What is a status code 308?

- A. A permanent redirect; This is the right code if the resource will now be available at a new URL and the client should directly access it via the new URL in the future. The current endpoint can’t control the clients’ behavior after the request and a subsequent redirect if the resource URL changes again have to be issued from the new URL.



- Q. What code would you use if an update didn’t return data to a client?

- A. 204


- Q. What code would you use if a resource used to exist but no longer does?

- A. 404


- Q. What is the ‘Forbidden’ status code?

- A. 403


