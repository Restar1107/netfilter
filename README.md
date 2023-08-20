# netfilter

1. prev, you need to put next instruction
install basic level
# sudo apt install libmnl-dev
# sudo apt install libnfnetlink-dev
# sudo apt install libnetfilter-queue-dev

Set your packet to flow through NFQUEUE
# sudo iptables -F
# sudo iptables -A OUTPUT -j NFQUEUE --queue-num 0
# sudo iptables -A INPUT -j NFQUEUE --queue-num 0

Make file
# gcc -o nfqnl_test nfqnl_test.c -lnetfilter_queue

2. ./nfqnl_test test.gilgil.net

3. open new terminal and try fallow instruction
# curl test.gilgil.net
