# a Plugin for Icinga2 to check the traffic on a specific interface using "vnstat". #

I searched high and low for something that would monitor the traffic ratee of network interfaces. I couldn't find something. So I decided to "roll my own", so to speak. Using bash. And I've never used bash before.

I took it as a challenge, since learning bash and doing something in it is something I've been wanting to do for some time now, so this seemed like a perfect opportunity.

I present to you the fruit of my labour. No doubt there are many things that can be done differently, or even better, but this is my first bash script, so sorry if there are some unnecessary things. **Please point them out if there are.**

----------
## Arguments: ##
- -w: Incoming Speed Warning
- -c: Incoming speed Critical
- -W: Outgoing speed Warning
- -C: Outgoing speed Critical
- -i: Interface this should monitor
- -p: Whether the script should provide performance data or not PLEASE NOTE: The more network interfaces present, the longer the check will take if Performance Data is neccesary to be retrieved.

## Note: ##
The units you specify the warnings/critical in must be units "KiB", otherwise the script will not work correctly, and eveything would give incorrect information.

When used on systems that uses comma separators in numbers(e.g. DE), please set the vnstat language to EN:

`vi /etc/vnstat.conf` (Ubuntu)
```
# locale (LC_ALL) ("-" = use system locale)
Locale "en_us.utf-8"
```

## Usage: ##
    ./check_traffic_vnstat.sh -w [incomingwarning] -W [outgoingwarning] -c [incomingcritical] -C [outgoingcritical] -i [interface] -p
## Extra Credit: ##
Thanks to 

- [AboutTimeIStoppedLurking](https://imgur.com/user/AboutTimeIStoppedLurking "AboutTimeIStoppedLurking's Imgur profile.")
- [karmalicious79](https://imgur.com/user/karmalicious79 "karmalicious79's Imgur profile.")
- [SendPotatoes](https://imgur.com/user/SendPotatoes "SendPotatoes's Imgur profile.")

on [www.imgur.com](www.imgur.com "www.imgur.com") for their helping me with this.
 
