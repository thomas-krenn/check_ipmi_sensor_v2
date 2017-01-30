Nagios / Zenos ipmi plugin: check_ipmi_sensor
=============================================


# Overview

This is a check for IPMI health of a server using freeipmi 0.8+. When used as a Nagios plugin performance data is generated where possible from ipmi values. It has minimal dependencies.

# How to run

    sudo ./check_ipmi_sensor -H localhost

# Dependencies

Freeipmi 0.8+
gawk

# Compatibility

Tested on Ubuntu Precise 64bit on various Dell hosts.

# Ignoring certain cases

Ignoring any drive failures monitoring via a check_raid plugin:-

    check_ipmi_sensor -O '--exclude-groups=Drive_Slot'

Ignoring specific sensors via an ignore file:-

    /etc/check_ipmi_sensor_ignore

    ...
    53;83
    ...



