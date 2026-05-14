# sync-prod-to-local

A bash script for syncing a remote WordPress database to a local database. This setup assumes your site is built with the Roots Bedrock framework.

## Setup and Usage

1. Add this script to your project. I typically place it within a `bin/` directory I create from the root of my Bedrock setup.
2. Add the below environment variables to your `.env`. Replace the `{$variable_name}` patterns with your configuration.
3. Call the script from the root of your locally hosted Bedrock site.

## Environment Variables

Add these constants to your `.env`:

```
# --- WP Sync (prod -> local) ---
SYNC_REMOTE_SSH_USER={$your_remote_user}
SYNC_REMOTE_SSH_HOST={$your_remote_ip}
SYNC_REMOTE_SSH_PORT=22

SYNC_REMOTE_HOST={$your_remotehost}
SYNC_LOCAL_HOST={$your_localhost}

# Bedrock web root on remote (where WP lives)
SYNC_REMOTE_WEB_DIR='{$your_remote_web_dir}'

# Remote staging dir for temp SQL + archive (must be writable)
SYNC_REMOTE_STAGE_DIR='{$your_remote_tmp_dir}'
```