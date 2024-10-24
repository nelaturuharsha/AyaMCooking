# AyaMCooking
🍳 AyaMCooking is a Voice-to-Voice Multi-lingual RAG Agent that makes a perfect sous chef for your kitchen, in upto 10 Languages 🤌🤗

In this notebook, we demo just one of the numerous capabilities enabled by a truly multilingual workflow as that which is enabled by Aya Expanse by Cohere For AI and Cohere.

Overall Objective:

People often would like to try a local cuisine, but the authentic recipes are often in the language of origin -- finding the ingredients, substitutes and other information is challenging and limits creativity.

- We first use Aya Expanse to generate recipe candidates, which is then used to generate recipes as well. This forms our dataset, which we subsequently embed at a later stage to form our index.

- But often, rather than typing a query and reading a recipe, you'd prefer if it was audio based - its just easier to follow with all the ingredients around, therefore we build a workflow where you can speak to Aya and get a response back in audio form.

- The pipeline uses Whisper to transcribe recorded audio across a wide variety, the textual question transcribed in the original language is then passed through a Multi-lingual RAG system where the index and embeddings are constructed using Cohere-multilingual-v3-Embed and for refinement, we use Cohere ReRank3.

- The context extract from the RAG, and our prompt, are combined with the language code and passed through Aya Expanse to generate a textual response. This is then used to generate a voice response using Coqui TTS in the language of the user's query.

- The multi-lingual capabilities allow us to extract recipes and information from various other languages, and provide context which can lead to some very creative recipe suggestions that are still grounded in local culture and taste.

The notebook is documented, and the only thing you'll need on your end is a bit of creativity, luck (the hope is the audio recording, GPU VM on colab etc., are readily available) and Cohere API key.

Have fun leveraging the power of open source!
Harsha | Bhavnick

## Citation 
```bibtex
@software{AyaMCooking,
    title        = {{AyaMCooking: A Voice-to-Voice Multilingual RAG bot for Cooking}},
    author       = {Minhas, Bhavnick and Nelaturu, Sree Harsha},
    year         = 2024,
    month        = 10,
    version      = {0.0.1}
}
```
