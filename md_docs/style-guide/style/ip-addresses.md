---
title: IP Addresses
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/ip-addresses/
---

# IP Addresses

An *IP address* uses a sequence of numbers to uniquely identify a particular computer on the Internet.

- When discussing IP addresses or referring to a specific IP address, don't use *IP* only; use *IP address*. You don't need to spell out *IP* on first use.

- When referring to a specific version of the IP, use *IPv4 address* or *IPv6 address* as appropriate.

## Types of IP Addresses

<table>
<tr>
<th id="Address%20Type">
Address Type

</th>
<th id="Notation">
Notation

</th>
<th id="Separator">
Separator

</th>
</tr>
<tr>
<td headers="Address%20Type">
IPv4

</td>
<td headers="Notation">
four groups of one to three decimal digits

</td>
<td headers="Separator">
periods (`.`)

</td>
</tr>
<tr>
<td headers="Address%20Type">
IPv6

</td>
<td headers="Notation">
eight groups of four hexadecimal digits

</td>
<td headers="Separator">
colons (`:`)

</td>
</tr>
</table>

## Examples

<table>
<tr>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Examples">
If your website is hosted in the `us_east_1` region, you can use the following primary and secondary IP addresses:

- Primary: 74.205.61.228

- Secondary: 74.205.61.229

- Additional: 72.32.36.144/28 (72.32.36.145 - 72.32.36.158)

</td>
</tr>
<tr>
<td headers="Examples">
Each Atlas cluster is assigned one public IPv4 address.

</td>
</tr>
<tr>
<td headers="Examples">
If you're using IPv6 on your host, you might need to add the IPv6 addresses of your name servers to the **resolv.conf** file.

</td>
</tr>
</table>

## Example IP Addresses for Documentation

If you need to show an example IP address, don't use one that is or might be assigned to an actual host. Use an address that's globally defined for documentation.

### IPv4 Addresses

RFC 5737 lists three valid IPv4 address CIDR blocks for documentation:

<table>
<tr>
<th id="Range">
Range

</th>
<th id="TEST-NET-1">
TEST-NET-1

</th>
<th id="TEST-NET-2">
TEST-NET-2

</th>
<th id="TEST-NET-3">
TEST-NET-3

</th>
</tr>
<tr>
<td headers="Range">
CIDR Block

</td>
<td headers="TEST-NET-1">
192.0.2.0/24

</td>
<td headers="TEST-NET-2">
198.51.100.0/24

</td>
<td headers="TEST-NET-3">
203.0.113.0/24

</td>
</tr>
<tr>
<td headers="Range">
First IP

</td>
<td headers="TEST-NET-1">
192.0.2.0

</td>
<td headers="TEST-NET-2">
198.51.100.0

</td>
<td headers="TEST-NET-3">
203.0.113.0

</td>
</tr>
<tr>
<td headers="Range">
Last IP

</td>
<td headers="TEST-NET-1">
192.0.2.255

</td>
<td headers="TEST-NET-2">
198.51.100.255

</td>
<td headers="TEST-NET-3">
203.0.113.255

</td>
</tr>
</table>

### IPv6 Addresses

RFC 3849 lists one valid IPv6 address prefix:

<table>

<tr>
<td>
IP Prefix

</td>
<td>
2001:DB8::/32

</td>
</tr>
<tr>
<td>
First IP

</td>
<td>
2001:0DB8:0000:0000:0000:0000:0000:0000

</td>
</tr>
<tr>
<td>
Last IP

</td>
<td>
2001:0DB8:FFFF:FFFF:FFFF:FFFF:FFFF:FFFF

</td>
</tr>
</table>

## Localhost or Loopback Address

One IP address in the IPv4 and IPv6 address ranges allow a host to communicate with itself. Use these IP addresses only when the text requires you to specify the localhost or loopback address.

<table>

<tr>
<td>
IPv4

</td>
<td>
127.0.0.1

</td>
</tr>
<tr>
<td>
IPv6

</td>
<td>
::1/128

</td>
</tr>
</table>

## Private vs. Public IP Address Spaces

Two other reserved IP address CIDR blocks exist for private networks not attached to the Internet. Hosts with IP addresses within these CIDR blocks cannot be accessed over the Internet.

Don't include these addresses in documentation. The user may be using an IP address in these ranges. This could result in an accidental copy and paste from the documentation to a user's environment. This section is provided for writers to identify these addresses as different from public IP addresses.

RFC 1918 lists three valid IPv4 address CIDR blocks for private networks:

<table>

<tr>
<td>
CIDR Block

</td>
<td>
10.0.0.0/8

</td>
<td>
172.16.0.0/12

</td>
<td>
192.168.0.0/16

</td>
</tr>
<tr>
<td>
First IP

</td>
<td>
10.0.0.0

</td>
<td>
172.16.0.0

</td>
<td>
192.168.0.0

</td>
</tr>
<tr>
<td>
Last IP

</td>
<td>
10.255.255.255

</td>
<td>
172.31.255.255

</td>
<td>
192.168.255.255

</td>
</tr>
</table>RFC 4193 lists one valid IPv6 address prefix for private networks:

<table>

<tr>
<td>
IP Prefix

</td>
<td>
fc00::/7

</td>
</tr>
<tr>
<td>
First IP

</td>
<td>
FC00:0000:0000:0000:0000:0000:0000:0000

</td>
</tr>
<tr>
<td>
Last IP

</td>
<td>
FDFF:FFFF:FFFF:FFFF:FFFF:FFFF:FFFF:FFFF

</td>
</tr>
</table>