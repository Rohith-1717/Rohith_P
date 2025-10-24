I had no time for this task 😭🙏, I did this few hrs before deadline

1) Question Answering:

-For question answering I used a roberta base model (version from deepset).
-It is fine tuned with a span-extraction dataset containing context, question, answer triplets. 
-Tokens for cls question (sep) context (sep) are fed into the transformer encoder.The model outputs contextual embeddings for each token.
-Two linear layers on top of the last hidden states produce start and end logits over all tokens.

2) French Translator

-Base Model is Helsinki-NLP/opus-mt-en-fr. It is a Marian Machine Translation model, based on the transformer encoder-decoder architecture.
-Source English sentences are tokenized into subword tokens using a Byte-Pair Encoding tokenizer.

So input is question and context, and it predicts start and end using the Question Anser Model (Questionanswermodelbetter).
English answer is encoded using translation tokenizer. 
French text is generated. Decode to get the final French answer.
