Functional Object Programming
=============================


**NAME**


    ``fop`` - FOP


**SYNOPSIS**


    | ``fopctl  <cmd> [key=val] [key==val]``
    | ``fopd`` 
    | ``fops``


**DESCRIPTION**


    FOP contains all the python3 code to program objects in a functional
    way. It provides a base Object class that has only dunder methods, all
    methods are factored out into functions with the objects as the first
    argument. It is called Object Programming (OP), OOP without the
    oriented.

    FOP allows for easy json save//load to/from disk of objects. It
    provides an "clean namespace" Object class that only has dunder
    methods, so the namespace is not cluttered with method names. This
    makes storing and reading to/from json possible.

    FOP has all you need to program a unix cli program, such as disk
    perisistence for configuration files, event handler to handle the
    client/server connection, deferred exception handling to not crash
    on an error, etc.

    FOP is Public Domain.

    1. You need to set PYTHONPATH if you run this locally.
    2. You might need to uninstall and rm ~/.cache/pip in case of error.


**INSTALL**

    installation is done with pipx

    | ``$ pipx install fop``
    | ``$ pipx ensurepath``
    |
    | <new terminal>
    |
    | ``$ fop srv > nixm.service``
    | ``$ sudo mv fop.service /etc/systemd/system/``
    | ``$ sudo systemctl enable fop --now``
    |
    | joins ``#fop`` on localhost


**USAGE**

    without any argument the bot does nothing

    | ``$ fop``
    | ``$``

    see list of commands

    | ``$ fop cmd``
    | ``cfg,cmd,dne,dpl,err,exp,imp,log,mod,mre,nme,``
    | ``now,pwd,rem,req,res,rss,srv,syn,tdo,thr,upt``

    start daemon

    | ``$ fopd``
    | ``$``

    start service

    | ``$ fops``
    | ``<runs until ctrl-c>``

    show request to the prosecutor

    | $ ``fop req``
    | Information and Evidence Unit
    | Office of the Prosecutor
    | Post Office Box 19519
    | 2500 CM The Hague
    | The Netherlands


**COMMANDS**

    here is a list of available commands

    | ``cfg`` - irc configuration
    | ``cmd`` - commands
    | ``dpl`` - sets display items
    | ``err`` - show errors
    | ``exp`` - export opml (stdout)
    | ``imp`` - import opml
    | ``log`` - log text
    | ``mre`` - display cached output
    | ``now`` - show genocide stats
    | ``pwd`` - sasl nickserv name/pass
    | ``rem`` - removes a rss feed
    | ``res`` - restore deleted feeds
    | ``req`` - reconsider
    | ``rss`` - add a feed
    | ``syn`` - sync rss feeds
    | ``tdo`` - add todo item
    | ``thr`` - show running threads
    | ``upt`` - show uptime


**CONFIGURATION**

    irc

    | ``$ fopctl cfg server=<server>``
    | ``$ fopctl cfg channel=<channel>``
    | ``$ fopctl cfg nick=<nick>``

    sasl

    | ``$ fopctl pwd <nsvnick> <nspass>``
    | ``$ fopctl cfg password=<frompwd>``

    rss

    | ``$ fopctl rss <url>``
    | ``$ fopctl dpl <url> <item1,item2>``
    | ``$ fopctl rem <url>``
    | ``$ fopctl nme <url> <name>``

    opml

    | ``$ fopctl exp``
    | ``$ fopctl imp <filename>``


**SOURCE**

    source is `here <https://github.com/otpcr/fop>`_


**FILES**

    | ``~/.fop``
    | ``~/.local/bin/fopctl``
    | ``~/.local/bin/fopd``
    | ``~/.local/bin/fops``
    | ``~/.local/pipx/venvs/fop/*``


**AUTHOR**

    | Bart Thate <``record11719@gmail.com``>


**COPYRIGHT**

    | ``FOP`` is Public Domain.
