README
######

Installation
************
Place the ``custom_components`` folder into your configuration directory
(or add its contents to an existing ``custom_components`` folder).

Authentication
**************
You will need to perform one-time authentication for the API to work.

.. code:: bash

    pip install hisensetv
    hisensetv 10.0.0.28 --authorize

See `newAM/hisensetv <https://github.com/newAM/hisensetv>`_ for more details.

Configuration
*************

.. code:: yaml

    media_player:
      - platform: hisensetv
        host: 10.0.0.28
        mac: ab:cd:ef:12:34:56
        name: tv
        model: TBD
        
    switch:
      - platform: hisensetv
        host: 10.0.0.28
        mac: ab:cd:ef:12:34:56
        name: tv
        model: TBD
        
Television Configuration
************************
-- The following settings must be altered

*************

.. code:: yaml

 Model: H9 (2019)
 
 -- Setting: Wake Up : Wake On LAN
 NOTE: If using Wireless, then use:
 -- Setting: Wake Up : Wake On Wireless Network
   


Advanced Commands
*****************
For advanced needs, additional commands, such as menu navigation, may be 
sent via the developer tools, under the 'Services' tab.

.. code:: bash

    select service 'hisensetv.send_command'
    click 'FILL EXAMPLE DATA' at bottom
    select Entity - must be HisenseTV device (media_player or switch)
    update command value, as desired
    
    
Warning
*******
This is provided **as-is**.
This is my first time going this deep into homeassistant and I have no idea
if I have horribly messed something up.

Future
*******
Determine if model functional is necessary for future model options
