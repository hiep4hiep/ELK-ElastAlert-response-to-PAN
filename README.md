# ELK-ElastAlert-response-to-PAN
ElastAlert python action to response to PANW Firewall

These files came as a pair:
- traps_malware.yaml: template to define an ElastAlert rule to run on your Elastic Stack. This will check for condition to match a specific log field then do an action to response when rule is hit.
- traps_malware_action.py: define a chain of actions that system will automatically execute when rule is hit, including:
  + Sending email
  + Sending Line message to notify admin
  + Query Palo Alto Networks AutoFocus threat intelligence for related artifacts/IOC of malware hash in threat log
  + Update IOC to Firewall to block further activity of malware
  

Installation:
- Put 2 files into ElastAlert rule folder
- Run this rule  or re-run whole ElastAlert

Happy threat response!
