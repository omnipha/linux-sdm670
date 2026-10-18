# linux-sdm670

Kernel tree for Qualcomm SDM670 devices: Google Pixel 3a / 3a XL (sargo/bonito)
and related, from [gitlab.com/sdm670-mainline/linux](https://gitlab.com/sdm670-mainline/linux).

## Branches
- `upstream` — read-only mirror of the upstream tree/tags. Never commit here manually.
- `omnipha` — our patches, rebased onto upstream tags. Contributions via PR against this branch.
- `main` — this documentation only.

## First patch (branch omnipha)
`ath: regd: default unprogrammed EEPROM to world regdomain with ch 12/13` —
units with unprogrammed EEPROM regdomain (0x0) get 2.4 GHz channels 12/13
permanently disabled; the patch maps 0x0 to WOR5_ETSIC (0x65) so country
regdomains like DE apply. Verified on Pixel 3a (sargo).

## Kernel policy
Upstream activity is tracked in [UPSTREAM.md](UPSTREAM.md). While upstream is active, Omnipha builds reference it and we push patches upstream when possible. If upstream goes inactive, `omnipha` becomes the maintained source of truth.

## License
GPL-2.0-only, same as upstream Linux.
