To send 0.0453 BTC from xmr.to just run this and follow the instructions:

    ./xmrto 1B1tAaf5x1HUXtCNLbtMDqxw6o5GNy4xqX 0.0453

To interface with and autopay from your Monero wallet:

    ./xmrto -a 1B1tAaf5x1HUXtCNLbtMDqxw6o5GNy4xqX 0.0453

Full usage:

    usage: xmrto [-h] [-P] [-S STATUS] [-E] [--addresses] [--unused] [-C LABEL]
                 [-B] [-R WALLET_REQUEST] [-K] [--churn] [-a]
                 [--rpc-host RPC_HOST] [--rpc-port RPC_PORT]
                 [--rpc-creds RPC_CREDS] [--rpc-login-file RPC_LOGIN_FILE]
                 [-m MAX_AUTOPAY] [-A ACCOUNT]
                 [--priority {auto,default,unimportant,normal,elevated,priority}]
                 [--mixins MIXINS] [--unlock-time UNLOCK_TIME] [-c MONERO_CONFIG]
                 [--no-monero-config] [--no-autostart-daemon]
                 [--daemon-config DAEMON_CONFIG]
                 [--daemon-data-dir DAEMON_DATA_DIR] [--daemon-arg DAEMON_ARG]
                 [--no-autostart-wallet-rpc] [-W WALLET] [-p WALLET_PASSWORD]
                 [--daemon-address DAEMON_ADDRESS] [--rpc-arg RPC_ARG]
                 [-f {USD,EUR,off}] [-n] [-D]
                 [address] [amount]
    
    positional arguments:
      address               Bitcoin address, Monero address, or Bitcoin payment
                            URL
      amount                Bitcoin or Monero amount as a decimal amount. Specify
                            min, max, or zeroconf to base the transaction amount
                            on the xmr.to min, max, and zero-conf maximums
                            respectively.
    
    optional arguments:
      -h, --help            show this help message and exit
    
    alternative actions:
      -P, --show-parameters
                            Show xmr.to parameters and exit
      -S STATUS, --status STATUS
                            Show status for a transaction (by UUID) and exit
      -E, --estimate        Show XMR estimate and exit (does not send the order
                            amount to xmr.to)
      --addresses           Get Monero wallet addresses and exit
      --unused              Get unused Monero wallet addresses and exit
      -C LABEL, --create-address LABEL
                            Make a new Monero wallet address for an account
      -B, --balances        Get Monero wallet balances and exit
      -R WALLET_REQUEST, --wallet-request WALLET_REQUEST
                            Run a Monero wallet RPC request and exit. Syntax:
                            --wallet-request "method?param1=value&param2=value"
      -K, --kill-daemons    Kill Monero daemons and exit
    
    churn options:
      --churn               Create a new address, send all funds to it
    
    autopay options:
      -a, --autopay         Try to automatically pay from a Monero wallet
      --rpc-host RPC_HOST   Monero wallet RPC host (default: 127.0.0.1)
      --rpc-port RPC_PORT   Monero wallet RPC port (default: 18083)
      --rpc-creds RPC_CREDS
                            Monero wallet RPC user:password (see monero-wallet-rpc
                            --rpc-login) (default: None)
      --rpc-login-file RPC_LOGIN_FILE
                            Monero wallet RPC .login file (default: None)
      -m MAX_AUTOPAY, --max-autopay MAX_AUTOPAY
                            Maximum BTC amount to autopay (use with monero-wallet-
                            rpc --rpc-login) (default: 4)
      -A ACCOUNT, --account ACCOUNT
                            Wallet account to pay from (index, tag, or label)
                            (default: auto)
      --priority {auto,default,unimportant,normal,elevated,priority}
                            Priority to send funds with (default: auto)
      --mixins MIXINS       Mixins to use with autopay (default: minimum of 10 and
                            the number xmr.to recommends)
      --unlock-time UNLOCK_TIME
                            Additional unlock time in blocks (actual time will be
                            N+10 blocks) (default: None)
    
    monero wallet config options:
      -c MONERO_CONFIG, --monero-config MONERO_CONFIG
                            Monero Wallet config file (default:
                            /home/admin/.config/monero-project/monero-core.conf)
      --no-monero-config    Do not use Monero config file
    
    autostart daemon options:
      --no-autostart-daemon
                            Do not try to start the monerod daemon
      --daemon-config DAEMON_CONFIG
                            Daemon config file
      --daemon-data-dir DAEMON_DATA_DIR
                            Daemon blockchain data directory (default: None)
      --daemon-arg DAEMON_ARG
                            Additional monerod daemon arguments
    
    autostart wallet RPC options:
      --no-autostart-wallet-rpc
                            Do not try to start monero-wallet-rpc
      -W WALLET, --wallet WALLET
                            Wallet .keys file (default: None)
      -p WALLET_PASSWORD, --wallet-password WALLET_PASSWORD
                            Wallet password (default: "")
      --daemon-address DAEMON_ADDRESS
                            Monero daemon to connect to (default: 127.0.0.1:18081)
      --rpc-arg RPC_ARG     Additional monero-wallet-rpc arguments. --rpc-bind-
                            port, --rpc-login, --wallet-file, and --password are
                            set for you.
    
    output options:
      -f {USD,EUR,off}, --fiat {USD,EUR,off}
                            Show fiat estimate during transaction with btcven
                            (does not send amount to the server) (default: USD)
      -n, --no-status       Do not wait for order to finish while showing status
                            info
    
    other options:
      -D, --debug           Show debug messages
