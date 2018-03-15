# ncbi-entrez-error-messages
A collection of error messages returned by NCBI Entrez

## Commonly asked questions

In this section I'll be trying to answer to the questions I expect people might have.

### Why do this?

I'm a long time user of the NCBI Entrez web service. It's a great service, but occasionally it fails.
Because the HTTP responses are usually streamed and go via a reverse proxy,
this means that when things fail on the NCBI side, the HTTP response header still says `220 OK`
while the transmitted data is breaking off mid-stream.

The proxy servers usually insert an error message, so the obvious thing to do
on the client side is to check for the presence of such a message.
That would all be fine if the error message was consistent, but unfortunately it isn't.
So here is a collection of all the different error messages I have seen from the NCBI
Entrez API.

### Shouldn't such a list be maintained by the NCBI

Yes, but I'm not aware of any NCBI documentation listing the possible error messages.

### I just got an error message that is not in the list

Please feel free to open an issue or submit a pull request to add the new message.

## License
I've added the Apache License to have a license on the repository.
For all I care, this license only applies to the README and FAQ.
The error_messages.txt file is a plain data collection that I make
available under a public domain dedication where available, or under a CC0
license otherwise.
