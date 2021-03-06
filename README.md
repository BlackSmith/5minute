5minute
=======

Give me an instance of mine image on OpenStack. Hurry!

QuickStart
----------

To run 5minute you need to install following libs:

    python3-keystoneclient
    python3-cinderclient
    python3-heatclient
    python3-neutronclient
    python3-novaclient
    python3-glanceclient
    python3-xmltodict
    python3-prettytable

To install them from RPMs (Fedora), please do `dnf -y install $( cat requirement-rpms.txt )`
or install RPM package from https://copr.fedorainfracloud.org/coprs/mkorbel/5minute/packages/
 
If you have installed 5minute using `pip install vminute`, they were installed as dependencies. Otherwise, you have to install them manually.

Get config file:

  1. Login into your OpenStack instance WebUI
  2. Navigate to Access & Security -> API Access
  3. Save file from "Download OpenStack RC File" to ~/.5minute/config

Get started:

  Show help:

    $ 5minute help

  Upload your SSH public key:

    $ 5minute key ~/.ssh/id_rsa.pub

  Show images we can work with:

    $ 5minute images

  Boot your machine (consider adding '--name' or '--flavor' to the command):

    $ 5minute boot <image_name_or_id>

  When the boot is finished, you should be able to ssh to your new machine

    $ ssh root@<machine_ip_address>

  You can list your current machines:

    $ 5minute list

  When you are done, kill the machine (you can do this via OpenStack webUI as well):

    $ 5minute delete <machine_name_or_id>

  To list available OpenStack scenarios:

    $ 5minute scenario templates

  Run scenario:

    $ 5minute scenario boot <scenario_template_name>

  When finished with the scenario, you should delete it:

    $ 5minute scenario delete <scenario_name_or_id>
