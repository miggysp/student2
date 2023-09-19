---
toc: True
comments: True
layout: post
title: Python Dictionary
courses: {'compsci': {'week': 5}}
type: hacks
---

```python
pip install PyDictionary

```

    Defaulting to user installation because normal site-packages is not writeable
    Requirement already satisfied: PyDictionary in c:\users\mihee\appdata\roaming\python\python311\site-packages (2.0.1)
    Requirement already satisfied: bs4 in c:\users\mihee\appdata\roaming\python\python311\site-packages (from PyDictionary) (0.0.1)
    Requirement already satisfied: click in c:\users\mihee\appdata\roaming\python\python311\site-packages (from PyDictionary) (8.1.7)
    Requirement already satisfied: goslate in c:\users\mihee\appdata\roaming\python\python311\site-packages (from PyDictionary) (1.5.4)
    Requirement already satisfied: requests in c:\users\mihee\appdata\roaming\python\python311\site-packages (from PyDictionary) (2.31.0)
    Requirement already satisfied: beautifulsoup4 in c:\users\mihee\appdata\roaming\python\python311\site-packages (from bs4->PyDictionary) (4.12.2)
    Requirement already satisfied: colorama in c:\users\mihee\appdata\roaming\python\python311\site-packages (from click->PyDictionary) (0.4.6)
    Requirement already satisfied: futures in c:\users\mihee\appdata\roaming\python\python311\site-packages (from goslate->PyDictionary) (3.0.5)
    Requirement already satisfied: charset-normalizer<4,>=2 in c:\users\mihee\appdata\roaming\python\python311\site-packages (from requests->PyDictionary) (3.2.0)
    Requirement already satisfied: idna<4,>=2.5 in c:\users\mihee\appdata\roaming\python\python311\site-packages (from requests->PyDictionary) (3.4)
    Requirement already satisfied: urllib3<3,>=1.21.1 in c:\users\mihee\appdata\roaming\python\python311\site-packages (from requests->PyDictionary) (2.0.4)
    Requirement already satisfied: certifi>=2017.4.17 in c:\users\mihee\appdata\roaming\python\python311\site-packages (from requests->PyDictionary) (2023.7.22)
    Requirement already satisfied: soupsieve>1.2 in c:\users\mihee\appdata\roaming\python\python311\site-packages (from beautifulsoup4->bs4->PyDictionary) (2.5)
    Note: you may need to restart the kernel to use updated packages.



```python
from PyDictionary import PyDictionary

#Initialize the PyDictionary
dictionary = PyDictionary()

#Function to fetch the meaning of a word
def fetch_meaning(word):
    try:
        meanings = dictionary.meaning(word)
        if meanings:
            for part_of_speech, definition_list in meanings.items():
                print(f"{part_of_speech}:")
                for definition in definition_list:
                    print(f"  - {definition}")
        else:
            print(f"Meaning not found for '{word}'")
    except Exception as e:
        print(f"An error occurred: {e}")

#Simple CLI interface for word lookup
while True:
    user_input = input("Enter a word to lookup (or 'exit' to quit): ").strip()

    if user_input.lower() == 'exit':
        break

    fetch_meaning(user_input)


```

    Adjective:
      - one or some or every or all without specification
    Adverb:
      - to any degree or extent

