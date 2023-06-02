# Assignment 2 

#### Objective: 

Understand token healing as implemented in Microsoft's GUIDANCE and create a standalone Python script to perform token healing on a given text.

#### Problem Statement:

Token healing is a technique used to correct errors in text by identifying and replacing incorrect or mistyped tokens with their intended correct forms. Microsoft's GUIDANCE is a system that implements token healing to improve the quality of text data. Your task is to study how token healing is implemented in GUIDANCE and create a Python script that can perform token healing on a given input text.

#### Microsoft's GUIDANCE - 

Language models process tokens, which are chunks of text that often are similar to a word. This impacts how language models see text, and also how we can prompt them since every prompt has to be a set of tokens. Encodings like BPE that are used by GPT-style models map all input bytes to token ids in a greedy manner. 
(Through approach 3 I have tried to work on this, but at the moment it is not giving accurate output.)

#### Problem Statement - 

The main aim of the Python scripts provided is to correct errors in the text by identifying and replacing incorrect or mistyped tokens with their intended correct forms.

# Approach 1 

## Token Healing using Dictionary

This Python script performs token healing by correcting misspelled words in a given input text. It utilizes a dictionary of correctly spelled words to replace misspelled tokens with their corresponding correct versions.

The script will perform token healing and display the original text, corrected text, and various statistics about the correction process.

### Functions

#### load_dictionary(file_path)

Loads the CSV file containing the misspelled words and their correct spellings. It returns a dictionary where the keys are misspelled words and the values are their correct versions.

#### perform_token_healing(text, dictionary)

Performs token healing on the given input text using the provided dictionary. It replaces misspelled tokens with their correct versions and returns the corrected text.

#### analyze_token_healing(original_text, corrected_text)

Performs analysis of the token healing process. It compares the original text with the corrected text and provides statistics such as the number of tokens, number of tokens corrected, and the correction rate. Additionally, it displays the incorrect tokens along with their corrected versions.


# Approach 2 

## Token Healing using Spacy

This Python script demonstrates the concept of token healing using Spacy, a popular natural language processing library, and a dictionary of misspelled words and their correct spellings. Token healing is a technique used to correct misspelled words or tokens in the text by replacing them with their correct spellings.

### Requirements

- Python 3. x
- Spacy
- CSV library

### Usage

1. Prepare a CSV file containing the misspelled words and their correct spellings. The CSV file should have two columns: "Misspelled Word" and "Correct Word". Each row represents a pair of misspelled and correct words. (Books1.csv)

2. Update the `csv_file_path` variable in the script with the file path to your CSV file.

3. Run the script.

4. Enter the input text when prompted.

5. The script will perform token healing on the input text using the provided dictionary and Spacy. It will print the original text, the corrected text, and various statistics related to the correction process.

### Functions

The script uses the load_dictionary function to load the misspelled words and their correct spellings from the provided CSV file. Make sure the CSV file is formatted correctly with the column headers "Misspelled Word" and "Correct Word".

The perform_token_healing function uses Spacy to process the input text and replace the misspelled tokens with their correct spellings.

The analyze_token_healing function provides additional analysis and statistics about the token healing process, such as the number of tokens, the number of tokens corrected, and the correction rate.

# Approach 3 (Still in progress)

### Token Healing with GPT-2
This Python script demonstrates the concept of token healing using the GPT-2 model from the Hugging Face transformers library. Token healing is a technique used to correct inconsistencies between the prompt and the generated text when using language models.

The perform_token_healing function takes a prompt and generated text as input. It first tokenizes the prompt and generated text using the GPT-2 tokenizer. Then, it checks if the first token of the generated text matches the last token of the prompt. If they don't match, it replaces the first token of the generated text with the last token of the prompt. Finally, it decodes the tokens back into text, resulting in a corrected version of the generated text.

To use this script, simply provide your prompt and generated text as inputs. The script will perform token healing and display the original prompt, generated text, and corrected text.

I am working on it right now, as it is not giving the correct output but I could work on iot only this much in 12 hours. 

# Approach 4 (Still in progress)

## Token Healing using Spell Checker

This Python script performs token healing by correcting misspelled words in a given input text. It utilizes the enchant library for spell checking and suggests replacements for misspelled words.

### Function

#### perform_token_healing(text)

Performs token healing on the given input text. It utilizes the enchant library to check for misspelled words and suggests replacements for them. The function tokenizes the text, checks each word, and replaces the misspelled words with the suggested corrections. Non-word tokens are kept as is. The corrected text is then reconstructed and returned.

### I am still working on approach 3 and 4. 




