ansible-clamav
==============

Installs clamav (daemon and client). 

Role Variables
______________

- `CLAMAV_SOCKET_TYPE`: The clamd daemon listens for incoming connections on
  Unix and/or TCP socket and scans files or directories on demand. This role
allows the clamd daemon to be configured with UNIX socket ("file") or TCP
socket ("tcp"). The default value is "file".
- `CLAMAV_MAX_FILE_SIZE`: Clamscan extracts and scans at most this number of
  kilobytes from each archive. You may pass the value in megabytes in format xM
or xm, where x is a number. This option protects your system against DoS
attacks (default: "2000M", max: <4GB)
- `CLAMAV_MAX_SCAN_SIZE`: Clamscan extracts and scans at most this number of
  kilobytes from each scanned file. You may pass the value in megabytes in
format xM or xm, where x is a number. This option protects your system against
DoS attacks (default: "2000M", max: <4G)
- `CLAMAV_MAX_STREAM_LENGTH`: Clamd uses FTP-like protocol to receive data from
  remote clients. This option allows you to specify the upper limit for data
size that will be transfered to remote daemon when scanning a single file.
(default: "2000M")

- `CLAMAV_TCP_PORT`: TCP port number the clamd daemon will listen on. (default:
  "3310")

- `CLAMAV_TCP_ADDR`: TCP socket address to bind to. (default: "127.0.0.1")

Author Information
------------------

Artefactual Systems
