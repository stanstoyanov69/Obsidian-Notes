There are many more ways to filter packets. After all, in any real-life situation, we would need to filter through thousands or even millions of packets. It is indispensable to be able to express the exact packets to display. For example, we can limit the displayed packets to those smaller or larger than a certain length:

- `greater LENGTH`: Filters packets that have a length greater than or equal to the specified length
- `less LENGTH`: Filters packets that have a length less than or equal to the specified length

We recommend you check the `pcap-filter` manual page by issuing the command `man pcap-filter`; however, for the purposes of this room, we will focus on one advanced option that allows you to filter packets based on the TCP flags. Understanding the TCP flags will make it easy to build on this knowledge and master more advanced filtering techniques.

### Binary Operations

Before proceeding, it is worth visiting binary operations. A binary operation works on bits, i.e., zeroes and ones. An operation takes one or two bits and returns one bit. Let’s explain in more depth and consider the following three binary operations: `&`, `|`, and `!`.