def word_freq(text):
    # Split text into individual words and convert to lowercase
    words = text.lower().split()

    # Create an empty dictionary to store word frequencies
    freq_dict = {}

    # Iterate through each word in the text
    for word in words:
        # Increment the frequency count for this word
        freq_dict[word] = freq_dict.get(word, 0) + 1

    # Sort the dictionary by frequency in descending order
    sorted_freq = sorted(freq_dict.items(), key=lambda x: x[1], reverse=True)

    # Create a list of tuples containing each word and its frequency count
    word_freq_list = [(word, freq) for word, freq in sorted_freq]

    return word_freq_list

