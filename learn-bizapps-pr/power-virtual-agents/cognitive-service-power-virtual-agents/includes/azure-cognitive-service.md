Azure Cognitive Service for Language is a cloud-based service that provides Natural Language Processing (NLP) features for understanding and analyzing text. This service helps build intelligent applications using the web-based Language Studio, REST APIs, and client libraries. This Language service unifies commonly used services such as Text Analytics, QnA Maker, and LUIS, and provides several new features.

These features can either be:

- **Pre-configured**: We made these pre-built AI models to be easily consumed, so they aren't customizable. You just send your data and use the feature's output in your applications.

- **Customizable**: Means that you train an AI model using the tools to fit your data specifically.

Azure Cognitive Service for Language lets you do many different things such as:

- **Extract information**: Use Natural Language Understanding (NLU) to extract information from unstructured text. For example, it can identify key phrases or Personally Identifiable Information (PII), summarize text, recognize and categorize named entities, or customize an entity extraction model on top of your domain set.

   > [!div class="mx-imgBorder"]
   > ![A screenshot of a key phrase extraction example.](../media/key-phrase.png)

- **Summarize text-based content**: Allows you to summarize lengthy documents and conversation transcripts.

   > [!div class="mx-imgBorder"]
   > [![A screenshot of a summarization example.](../media/summary.png)](../media/summary.png#lightbox)

- **Classify text**: Use NLU to detect the language or classify the sentiment of text you've. You can also classify your text documents by customizing a classification model over your dataset.

   > [!div class="mx-imgBorder"]
   > ![A screenshot of a language detection example.](../media/language.png)

- **Answer questions**: Provide answers to questions being asked in unstructured texts using the prebuilt capabilities, or customize your domain specific question-and-answer pairs over data you provide.

   > [!div class="mx-imgBorder"]
   > ![A screenshot of a question answering example.](../media/question-answer.png)

- **Understand conversations**: Create your own models to classify conversational utterances and extract detailed information from them to fulfill scenarios.

   > [!div class="mx-imgBorder"]
   > [![A screenshot of a conversational language understanding example.](../media/intent.png)](../media/intent.png#lightbox)

- **Translate text**: Use cloud-based machine translation to build intelligent, multi-language solutions for your applications.

Many of the features associated with the above-mentioned items can be easily used by Power Virtual Agent bots to help make the bot more efficient and allow it to handle various scenarios.

Some of the items available include:

- **Entity linking**: Identifies and extracts entities found in text. For example, in the sentence "*We went to Seattle last week.*", the word "*Seattle*" would be identified, with a link to more information on Wikipedia. For more information, see [Entity linking](/azure/cognitive-services/language-service/entity-linking/overview/?azure-portal=true)

- **Named entity recognition**: Identifies and categorizes entities in unstructured text such as people, places, organizations, and quantities. For more information, see [Named entity recognition](/azure/cognitive-services/language-service/named-entity-recognition/overview/?azure-portal=true)

- **Sentiment**: Helps find out what people think of your brand or topic by mining text for clues about positive or negative sentiment. It can associate the positive and negative sentiment with specific aspects of the text. For more information, see [Sentiment analysis and opinion mining](/azure/cognitive-services/language-service/sentiment-opinion-mining/overview/?azure-portal=true)

- **Detect language**: Detects the language a document is written in, and returns a language code for a wide range of languages, variants, dialects, and some regional/cultural languages. For more information, see [Language detection](/azure/cognitive-services/language-service/language-detection/overview/?azure-portal=true)

- **Detect personal information**: Can identify, categorize, and redact sensitive information in unstructured text such as phone numbers, email addresses, and forms of identification. For more information, see [Personally Identifiable Information (PII) detection](/azure/cognitive-services/language-service/personally-identifiable-information/overview/?azure-portal=true)

- **Key phrases**: Quickly identifies the main concepts in text. For example, in the text "*The food was delicious and the staff were wonderful.*", key phrase extraction will return the main topics of "*food*" and "*wonderful staff*". For more information, see [Key phrase extraction](/azure/cognitive-services/language-service/key-phrase-extraction/overview/?azure-portal=true)

For example, you could use the detect personal information feature to analyze information in a conversation to extract a phone number, email address, or street address. This information could be based to other services such as your organizations Customer Relationship Management (CRM) system to identify the corresponding customer record. Once you've identified the appropriate record, all the information associated with that customer in your CRM application could be made available to your PVA bot to use. This allows you to create a more personalized experience.

For the remainder of this module, we're going to focus on how to configure a PVA bot to use Azure Cognitive Service for Language in the bot. However, if you're interested in learning how to create some of these elements using Azure Cognitive Service for Language, you can find more information in the resources below:

- [What is Azure Cognitive Service for Language](/azure/cognitive-services/language-service/overview/?azure-portal=true)

- [Getting started with Language Studio](/azure/cognitive-services/language-service/language-studio/?azure-portal=true)

- [Build customer question answering models](/azure/cognitive-services/language-service/question-answering/overview/?azure-portal=true)

- [Responsible use of AI](/legal/cognitive-services/language-service/transparency-note?context=%2Fazure%2Fcognitive-services%2Flanguage-service%2Fcontext%2Fcontext&azure-portal=true)
