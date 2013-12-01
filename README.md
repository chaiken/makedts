makedts
=======

Makedts is bash script that invokes the C preprocessor and device-tree
compiler to transform a nested hierarchy of device-tree source files
into a single human-readable ASCII output.  Many mistakes in DTS
are obvious from inspection of the script's output: some node is at the
wrong level of the hierarchy, or has an empty property that was
expected to be populated. A working similar device-tree binary can be
compared by running fdtdump (in the kernel source's scripts/dtc) on
the binary and lining up the forward-compiled failure with the
reverse-compiled working DTB.

makedts produces a similar result to fdtdump's output on a matching
DTB, but with the advantage of having ASCII-formatted strings rather
than hex ones. 

See previous discussion at https://lwn.net/Articles/573409/ and http://www.spinics.net/lists/devicetree/msg08941.html.
