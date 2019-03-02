# factorio_server_scripts
Scripts for installing and updating factorio on a ubuntu server

To use.

Clone the repo onto the server.
cd to the cloned repo
Run `./scripts/install_update_factorio --install`

This will install the latest experimental factorio version
It will be set to start on boot but will not start immediately
A default save file and settings must be changed before it can start.

It also installs a cronjob that runs at about midnight AEST that checks for a update
If one exists it stops the server, upgrades it and restarts it.

It takes a backup copy of the save file before doing this but you may still lose data.
Factorio only saves to disk on a interval, default 10 minutes, editable in the config.
