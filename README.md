# Stop forwarding locale from the client.
Do not forward the locale environment variable from your local machine to the server. You can comment out the SendEnv LANG LC_* line in the local /etc/ssh/ssh_config file.

# Stop accepting locale on the server.
Do not accept the locale environment variable from your local machine to the server. You can comment out the AcceptEnv LANG LC_* line in the remote /etc/ssh/sshd_config file.

# Forward port from your localhost to remote localhost.
ssh -L 123:localhost:456:remotehost

# Forward port from remote host to your localhost.

# Reference
* https://askubuntu.com/questions/144235/locale-variables-have-no-effect-in-remote-shell-perl-warning-setting-locale-f
* https://unix.stackexchange.com/questions/115897/whats-ssh-port-forwarding-and-whats-the-difference-between-ssh-local-and-remot
