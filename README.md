# Vault Server

This is a container running Vault by HashiCorp. It is based on alpine linux,
and uses gpg and shasums to verify the vault binary used. This is to ensure
the security of the vault by preventing a modified vault binary.


## Running

To run this container, use

    docker run -it -p 8200:8200 --hostname vault --name vault tritlo/vault


To run with a given config (assuming it is in the `config/config` ) run:


    docker run -it -p 8200:8200 --hostname vault --name vault \
        -v $PWD/config/config.hcl:/config/config.hcl tritlo/vault server --config=/config/config.hcl

## More info

More info on vault and it's usage can be found on [Vault by HashiCorp](https://www.vaultproject.io/)s project page

