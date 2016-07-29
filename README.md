# chunkyMonkey
Completely useless toy for experimenting with chunked encoding.

The server, `bin/chunkyMonkeyServer`, is a non-daemon, multi-thread command
line program.  It will only server up a single file, specified when started.
Terminate it with control-C or kill.  Run with `--help` for details.
Note, due to the complete lack of security evaluation of the code, the
server will only run on `localhost` unless `--public` is specified.

The program `bin/chunkyMonkeyClient` is used as a download demo, show
that no special code is required for using chunked transfer encoding
in Python.  Run with `--help` for details.

Examples of downloading from this server from the command line:
``` shell
wget --content-disposition http://localhost:20000
curl -J -O http://localhost:20000/
```

