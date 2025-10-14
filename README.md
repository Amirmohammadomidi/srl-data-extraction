# Semantic Role Labeling (SRL) Data Extraction

This repository contains the code for extracting and processing Semantic Role Labeling (SRL) data from the Wall Street Journal (WSJ) section (Chosen as a proof of concept) of the OntoNotes 5.0 corpus, as described in our research paper. 

## Methodology 

The data extraction process leverages annotations from the PropBank release and syntactic structures from the Penn Treebank. The scripts in this repository perform the following key steps: 

1.  **File Identification and Parsing:** Iterates through the WSJ sections of the OntoNotes corpus to identify and parse `.prop` files containing predicate-argument structures. 
2.  **Proposition and Sentence Extraction:** Extracts propositions, plain sentences, and Treebanked sentences from the `.prop` and `.onf` files. 
3.  **Annotation-Tree Index Mapping:** Establishes a mapping between the extracted propositions and their corresponding syntactic trees. 
4.  **Annotation Extraction and Conversion:** Extracts individual role annotations (ARG0, ARG1, REL) and converts them into textual spans. 
5.  **DataFrame Creation:** Organizes the extracted data into a Pandas DataFrame and exports it to a CSV file. 

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.
