# moco2jira

## Getting started

Clone this repo and add the transfer-File to your .zprofile or similar.

```
export M2J_ARRAY_OFFSET=1
export M2J_JIRA_TOKEN={{Your Jira Token}}
export M2J_JIRAS=('{{subdomain1}}' '{{subdomain_2}}')
export M2J_MOCO_API_KEY={{Your Moco API Key}}
export M2J_MOCO_SUBDOMAIN={{moco-subdomain}}
export M2J_USER={{Your email address}}

source ~/moco2jira/transfer
```

## Keep tracking

Keep Tracking your work in moco with the description
#TICKET work

e.g. `#TICKET-1234 code review`

After tracking you can transfer the booking to Jira by running
```
m2j
```

### Transfer tracking for another day

```
m2j -d 2024-01-01
```

### Delete tracking in Jira
It will only delete Tickets stated in Moco. It will not delete all

```
m2j --delete
m2j -d 2024-01-01 --delete
```

### Requirements
```
brew install jq
```
### Api-Keys

Moco => https://{{moco-subdomain}}.mocoapp.com/profile/integrations

Jira => https://id.atlassian.com/manage-profile/security/api-tokens
