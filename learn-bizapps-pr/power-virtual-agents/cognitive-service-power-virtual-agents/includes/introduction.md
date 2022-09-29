Organizations are always looking for ways to provide better service to their customers, and improve overall customer satisfaction. One way to do this is through conversational bots. Bots can help reduce the load on live agents by allowing incoming conversations on different channels to be routed to a bot first. They can assist the customer by walking them through some basic troubleshooting. If needed, the bot can escalate the conversation to a live agent who could further assist the customer in their journey.

Power Virtual Agents (PVA) allows you to create powerful AI-powered chatbots to assist with a range of requests, from providing simple answers to common questions, to resolving issues requiring complex conversations. With Power Virtual Agents, bots can be easily created without the need for data scientists or developers. This helps reduce the amount of time it takes an organization to deploy a bot solution. A Power Virtual Agent bot contains multiple topics. Think of a topic as a way of representing a question or item the bot can assist with.

A topic contains two primary items:

- **Trigger**: Represents keys words and phrases that can be input by a user that help the system identify which topic to use.

- **Conversation Path**: A series of messages, actions, and other items that guide the customer through the topic.

For example, an organization might create a topic related to returning items. When a customer asks how to return an item, the system will recognize the text in the trigger. It then uses the conversation path associated with that topic to provide guidance to the user and help them with their issue.

The text the user provides is compared against the different trigger phrases for all the topics defined in the bot to find the most relevant topic. While a trigger phrase doesn't need to match exactly what the user typed, the system still needs to compare what the user provided against all the triggers to find the right topic. Based on the complexity of your bot, you may create hundreds of different topics. Not only can this be time consuming to create, but it can also be challenging when there might be important information in there, but it's not something that's identified in a trigger. For example, personal identifying information such as phone number and addresses might be needed to help identify the right customer record in other systems your organization uses. To handle these types of scenarios, organizations can integrate other services into a Power Virtual Agent bot.

One cloud-based service that can help with this, is Azure Cognitive Services for Language. It can be used in PVA bots to provide necessary tools to take your bots to the next level. Throughout this module, we'll be walking you through how to use Azure Cognitive Services of Language in your PVA bots.

Before we get into the specifics on how to do this, lets first examine what Azure Cognitive Services for Language is.
