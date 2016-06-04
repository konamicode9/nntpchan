set up the daemon:

    ./srndv2 setup

generate admin keys, don't loose them.

    ./srndv2 tool keygen

add yourself as admin by adding your ``public key`` to the ``frontend`` section of ``srnd.ini``

    ...
    [frontend]
    enable=1
    admin_key=yourpublickeygoeshere
    ... # leave the rest of the config values alone for now

    

run it:

    ./srndv2 run


Now open the browser up to http://127.0.0.1:18000/

To access the mod panel go to the [mod panel](http://127.0.0.1:18000/mod/) and use your ``private key`` to log in

Now read about [peering](feeds.md)
