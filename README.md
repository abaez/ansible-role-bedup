ansible-role-bedup
=========
[![license][2i]][2p]
[![twitter][3i]][3p]

An ansible install of [bedup] for [btrfs].

Description
-----------

When using [btrfs], it can be quite useful to have [deduplication][4] at ease. The [bedup] program allows to use the already excellent abilites of [btrfs] to have [deduplication][4].

Role Variables
--------------

There are only two variables for the role and are optional for change. The two variables are:

``` yaml
bedup.tmp: /tmp/bedup # the temporary checkout location of bedup.
bedup.ver: v0.10.1 # the current version of bedup.

```

Requirements
------------

The only requirement is to have [btrfs] as a filesystem for the machine being provisioned.

Usage
-----

You can run the role by simply adding it to your playlist, like so:

``` yaml
- hosts: servers
    roles:
        - abaez.bedup
```

Author Information
------------------

[Alejandro Baez][1]

[bedup]: https://github.com/g2p/bedup
[btrfs]: https://btrfs.wiki.kernel.org/index.php/Main_Page

[1]: https://keybase.io/baez
[2i]: https://img.shields.io/badge/license-BSD_2-green.svg
[2p]: ./LICENSE
[3i]: https://img.shields.io/badge/twitter-a_baez-blue.svg
[3p]: https://twitter.com/a_baez
[4]: https://en.wikipedia.org/wiki/Data_deduplication
