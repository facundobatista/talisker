.. highlight:: python



==================
Request Id Tracing
==================

Basically, talisker will add request id data to every where it might be useful.
This includes:

  * in all log messages generated by that request
  * in outgoing HTTP requests using talisker requests Session
  * in the WSGI environ ('REQUEST_ID')
  * in the raven error data  (TODO)

This is implemented using werkzeug.locals, to provide thread/greenlet local storage.

