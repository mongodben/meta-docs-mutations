---
title: Time
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/time/
---

# Time

You can show time by using either the 24-hour or 12-hour clock.

- The 24-hour clock is the preferred format for international audiences and the format used in most computer systems, so use the 24-hour clock when possible.

- If the technology or interface that you're documenting shows or uses the 12-hour clock, then be consistent with the interface and use the 12-hour clock.

## 24-hour Clock

When you use the 24-hour clock to show time, use the following guidelines:

- Use a colon to separate the hours, minutes, and seconds.

- Show the hours, minutes, and seconds with two digits each, even if the leading digit is 0.

- If you need to show a time zone, use Coordinated Universal Time (UTC), and indicate the time-zone offset from UTC.

<table>
<tr>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Examples">
08:29:37

</td>
</tr>
<tr>
<td headers="Examples">
18:30:59

</td>
</tr>
<tr>
<td headers="Examples">
18:00:00 to 20:30:00

</td>
</tr>
<tr>
<td headers="Examples">
10:30:00 (UTC -6) (refers to CT)

</td>
</tr>
<tr>
<td headers="Examples">
12:00:00 (noon)

</td>
</tr>
<tr>
<td headers="Examples">
00:00:00 (midnight)

</td>
</tr>
</table>

## 12-hour Clock

When you use the 12-hour clock to show time, use the following guidelines:

- Use a colon to separate the hours and minutes. If the minutes are 00, you don't need to show them unless you're showing a span of time that includes a time with minutes.

- Use uppercase letters for abbreviations of ante meridiem (AM) and post meridiem (PM). Separate these abbreviations from the time with a space. Do not use periods in the abbreviations.

- When specifying time zones, show both the spelled-out name and the abbreviation. Show the name in lowercase letters; use uppercase letters and no periods for the abbreviation.

- Avoid references to standard and daylight saving time because the appropriate designation changes frequently. However, if you need to include such a reference, insert *S* (for standard) or *D* (for daylight) as the second character in the abbreviation.

- When referring to 12 AM, use *12 midnight* or just *midnight*. When referring to 12 PM, use *12 noon* or just *noon*.

<table>
<tr>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Examples">
10:29 AM

</td>
</tr>
<tr>
<td headers="Examples">
6 PM

</td>
</tr>
<tr>
<td headers="Examples">
6:00 PM to 8:30 PM

</td>
</tr>
<tr>
<td headers="Examples">
10:30 AM Central Time (CT)

</td>
</tr>
<tr>
<td headers="Examples">
1:30 PM Central Standard Time (CST)

</td>
</tr>
<tr>
<td headers="Examples">
midnight

</td>
</tr>
</table>