# C4 contest results setup checklist:
- [ ] Using this repo as a template, create a new private repo where contest finding reports will go (`sponsorname-results`)

Configure the contest report form in Netlify:
- [ ] Go to app.netlify.com » create new site (from GitHub)
- [ ] Choose `reporter` repo. Select advanced options.
- [ ] Add env variables, changing the contest #, sponsors, and repo like so:
```
REACT_APP_C4_CONTEST=1
REACT_APP_C4_SPONSOR=“Slingshot”
GITHUB_OWNER="code-423n4"
GITHUB_REPO=“slingshot-results"
GITHUB_TOKEN=“ADD-C4-TOKEN-HERE”
MAILGUN_KEY=“ADD-MAILGUUN-TOKEN-HERE”
MAILGUN_DOMAIN="mg.code423n4.com"
```
- [ ] Click **deploy site**
- [ ] Click **site settings** » **change site name** change netlify site name to `c4-{sponsor}` (so the contest form will be c4-sponsor.netlify.app)

C4 public repo checklist:
- [ ] Rename contest H1 below
- [ ] Add link to report form in contest bullets below
- [ ] Update pot sizes and start and end times in contest bullets below (ensure the total and dates match the [code423n4.com public contest data here](https://github.com/code-423n4/code423n4.com/tree/main/data/contests))
- [ ] In Discord, send the sponsor contact the url for this repo to follow the instructions below and add contracts here.
- [ ] Delete this checklist and await PR with GitHub handles to add to the public and private contest repos.

# Sponsorname Contest
- XXX main award pot
- XXX gas optimization award pot
- Join [C4 Discord](https://discord.gg/EY5dvm3evD) to register
- Submit findings [using the C4 form](https://c4-XXXXXXXX.netlify.app/)
- [Read our guidelines for more details](https://code423n4.com/compete)
- Starts XXX XXX XX 00:00 UTC
- Ends XXX XXX XX 23:59 UTC

This repo will be made public before the start of the contest.

---

## :handshake: Sponsors: Step By Step
Each contest uses two repos: a public one (this one) and a _private_ one where issues are submitted using the contest form. The private contest repo will be made public after the contest has been judged and identified issues are mitigated by the sponsor team.

Here's your part in getting the contest ready to go and joining the private repo.

- [ ] Fork the public repo for your contest. (This one.)
- [ ] Modify this `README.md` file to describe how your code is supposed to work with links to any relevent documentation and any other criteria/details that the C4 Wardens should keep in mind when reviewing.
- [ ] Add all of the code to this repo that you want reviewed.
- [ ] Make sure your code is thoroughly commented using the [NatSpec format](https://docs.soliditylang.org/en/v0.5.10/natspec-format.html#natspec-format).
- [ ] Create a PR with the above changes.
- [ ] In your repo, list the GitHub handles to be added to the private contest repo.

Please have contracts and documentation added to this repo **no less than 8 hours prior to contest start time.**
