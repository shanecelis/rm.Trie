csharp-trie
===========

A trie (prefix tree) data structure implementation in C#.

### Methods

```c#
// Add a word to the Trie.
void AddWord(string word);

// Get all words in the Trie.
ICollection<string> GetWords();

// Get words for given prefix.
ICollection<string> GetWords(string prefix);

// Returns true or false if the word is present in the Trie.
bool HasWord(string word);

// Returns the count for the word in the Trie.
int WordCount(string word);
```

### Example

```c#
// Create a new trie.
ITrie trie = TrieFactory.GetTrie();

// Add words.
trie.AddWord("test");
trie.AddWord("this");

// Get all words.
var allWords = trie.GetWords();

// Get words for a prefix.
var tePrefixWords = trie.GetWords("te");

// Check if a word is present.
var hasWord = trie.HasWord("test");

// Get word count for a word.
var wordCount = trie.WordCount("test");
```

#### Note: 

Not thread-safe.