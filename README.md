# LetsEncrypt Certbot-cli Certificate Generator Helper


## Generate 'certbot' cli command to create a certificate for a set of arbitrary FQDN or wildcard DNS domains


Certbot cli tool allows for manual generation of certificates using a 'manual' workflow. 

During the execution of the certbot command, the user is provided with a DNS TEXT record challenge that must be registered with your DNS provider before advancing.

For each domain requested, the certbot command provides a

`_acme_callenge.[domain-to-register]`

text record registration request along with at a unique value.


Once you 'hit-enter' LetsEncrypt will query for these DNS TXT records and if found, will generate a 90day TLS certificate containing the appropriate common name and SAN fields populated accordingly.


