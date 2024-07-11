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

Keep tracking your work in moco with the description
#TICKET work

e.g. `#TICKET-1234 code review`

After tracking you can transfer the tracking to Jira by running
```
m2j
```

### Transfer trackings to Jira for a different day
Use the `--day` or `-d` option to specify any date in the format YYYY-MM-DD.

```
m2j -d 2024-01-01
m2j --date 2024-01-01
```

### Delete tracking in Jira
It will only delete trackings for JIRA tickets stated in Moco. It will not delete all time-trackings you (manually) made in JIRA.
Trackings in Moco will never be deleted, as they count as single source of truth.

```
m2j --delete # delete JIRA time-trackings for today
m2j -d 2024-01-01 --delete # delete JIRA time-trackings for the spedified date
```

### Verbosing
```
m2j --verbose
m2j -v
```

### Requirements
```
brew install jq
```
### Api-Keys

Moco => https://{{moco-subdomain}}.mocoapp.com/profile/integrations

Jira => https://id.atlassian.com/manage-profile/security/api-tokens
