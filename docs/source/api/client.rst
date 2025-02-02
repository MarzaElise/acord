.. meta::
   :title: Documentation - Acord [Client]
   :type: website
   :url: https://acord.readthedocs.io/api/client.html
   :description: Base client for interacting with API
   :theme-color: #f54646

.. currentmodule:: acord

******
Client
******
ACord's built in client enables rapid development, but this doesn't mean you cant create your own!

Example
~~~~~~~

.. code-block:: py

    from acord import Client, Message
    from typing import Any

    class MyClient(Client):
        async def on_message(self, message: Message) -> Any:
            if message.content == ".ping":
                return message.reply(content="Pong!")
    
    if __name__ == "__main__":
        client = MyClient(token="My token")
        client.run()

Client
~~~~~~

.. attributetable:: Client

.. autoclass:: Client
    :members:
