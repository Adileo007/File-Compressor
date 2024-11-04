Algorithm
Huffman coding is a greedy algorithm that optimizes file compression by using variable-length encoding. The main steps are:

Frequency Analysis: Count the frequency of each character in the input file.
Build a Huffman Tree: Create a binary tree where characters with higher frequencies have shorter binary codes.
Encoding: Traverse the tree to assign binary codes to each character. Replace characters in the file with their corresponding binary codes to create a compressed file.
Decoding: Use the Huffman Tree to translate binary codes back to the original characters.
Project Structure
python
file-compressor/
├── src/
│   ├── main.cpp             # Main file for encoding and decoding
│   ├── huffman_encoding.cpp  # Implementation of Huffman encoding
│   ├── huffman_decoding.cpp  # Implementation of Huffman decoding
│   └── huffman_utils.cpp     # Helper functions
├── data/
│   ├── inputFile.txt         # Sample input file
│   ├── outputFile.bin        # Compressed output file
│   └── decodedOutput.txt     # Decoded file (matches original input)
├── README.md                 # Project README
└── LICENSE                   # License information
Installation
Clone this repository:
git clone https://github.com/username/file-compressor.git
cd file-compressor
Compile the source code using a C++ compiler:
g++ -o file_compressor src/main.cpp src/huffman_encoding.cpp src/huffman_decoding.cpp src/huffman_utils.cpp
Usage
Place the file you want to compress in the data folder as inputFile.txt.

Run the compiled program:
./file_compressor
The program will generate two files:

outputFile.bin - The compressed binary file.
decodedOutput.txt - The decompressed file (should match inputFile.txt).
Example
Suppose inputFile.txt contains:
This is an example text for Huffman coding.
Running the program will produce a compressed file (outputFile.bin). Decoding it will regenerate the original text in decodedOutput.txt.

Limitations
Text-Only Compression: This implementation currently only supports text files.
No Encryption: The compressed file is not encrypted and can be decoded by anyone with the Huffman tree data.
License
This project is licensed under the MIT License. See the LICENSE file for details
