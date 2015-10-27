l2fwd with simple protocol decoding and pattern matching by hyperscan.

This demo is used for testing throughput performance with different-scale
hyperscan databases with 1 lcore(work thread).

dependencies:

1. modify headroom of m_buf;
2. hyperscan.

compile:

LDFLAGS += -lhs
CC = g++ // yeah, if using gcc cause hyperscan link error.

run:

./l2fwd -c 3 -n 2 -- -p 3 -q 2 --ptn /path/to/ptn.txt
