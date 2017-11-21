# PREREQUISITES
- Run in Python 3

- Install both requests & Meraki Dashboard API Python modules:
`pip[3] install requests [--upgrade]`
`pip[3] install meraki [--upgrade]`

# DESCRIPTION
This script finds all MV cameras with a specified tag, and then iterates
through all networks to apply an exisitng group policy (enforced by the MX)
to the applicable cameras as client devices.

# USAGE
python mv_gp.py -k <api_key> -o <org_id> -t <tag> -p <policy> [-m <mode>]
The -t parameter specifies the required tag that needs to be present on the MV
camera, and -p the name of the MX group policy to be applied.
The optional -m parameter is either "simulate" (default) to only print changes,
or "commit" to also apply those changes to Dashboard.
