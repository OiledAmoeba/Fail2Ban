# Fail2Ban
* File: **xarf-login-attack.local**\
This is an add-on for the existing xarf-login-attack action in Fail2Ban.\
With this addon you can create a ticket in OTRS from inside Fail2Ban and include the ticket number in the XARF-Mail to easy track reactions.\
This addon uses `curl` to build the JSON string on the fly so no JSON has to be installed.\
*Requirements:*
  * `dig` (also required for the main action, if needed: included in `dnsutils`)
  * `base64` (included in `coreutils`)
  * `curl`
  * OTRS (tested on OTRS 6.0 CE)
  * OTRS-Webservice as "Provider", Type HTTP::REST (see the [OTRS manual](https://doc.otrs.com/doc/manual/admin/6.0/en/html/genericinterface.html#genericinterface-webservices) for a working Webservice example)
