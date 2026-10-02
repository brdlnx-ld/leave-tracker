# LCY8 Leave & Rota

Open https://brdlnx-ld.github.io/leave-tracker/ to use the current tracker. The original address automatically redirects to `/v2/`.

## Workspaces

- Members: their own leave, VET interest and published rotas.
- Trainers/admins: team leave, draft rota planning and publishing, VET requests and confirmations, team and individual trainer account management, and Slack notification settings.

Sign in with your individual account. Initial access codes must be changed at first sign-in. Trainers can create colleague accounts from the Trainers page.

The frontend is hosted on GitHub Pages in this repository. The backend is the LCY8 Leave Tracker Supabase project in the existing organisation on the Free plan. Real data and all server credentials stay out of this public repository. Never upload private access guides or migration backups here.

## Rota publishing and VET

Saving a draft does not change the member view. Publish each week and shift when ready. Imported historical rota records remain drafts until explicitly published. VET interest requires trainer confirmation; confirmed assignments enter the draft rota.

## Slack

Slack notification code is deployed but unconnected and off. Connect an incoming webhook for the chosen channel through the backend server secret `SLACK_WEBHOOK_URL`, then refresh the tracker and configure defaults in the Slack page. Never put the webhook into this repository. Notifications can be sent on rota publication or new VET requests. Draft saves do not send messages.

## Old backend retirement

The original homepage has been replaced by a redirect. The Google Sheet is retained as a backup. Its final records were checked against the new database on 2 October 2026. Owner action to archive the old Apps Script web-app deployments is still pending; until archived, cached old tabs could still reach that backend. Do not use the old tracker or edit the old Sheet for normal work. Recheck for late changes after archiving.

## Development

The six app files are under `v2/`. Changes to `main` deploy through GitHub Pages. Use sample mode to test with fictional people without database writes or Slack messages:

- Trainer: https://brdlnx-ld.github.io/leave-tracker/v2/?demo=1
- Member: https://brdlnx-ld.github.io/leave-tracker/v2/?demo=1&role=member

The prior frontend can be recovered from Git history. Keep regular private data backups using Export backup from the trainer account menu. Free Supabase projects may pause after low activity.
