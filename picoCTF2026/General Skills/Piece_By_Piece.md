# Piece by Piece

**Category:** General Skills  
**Points:** 50

### 1. Challenge Description

Multiple split file parts are present in the home directory. They need to be combined into a zip archive and extracted using a provided password to reveal the flag.

### 2. My Approach

- **Initial Thought:** Used `file` on each part to understand what they were — `part_aa` was identified as a zip archive, the rest as raw data, indicating a split file.
- **Research:** Recognised that all parts needed to be concatenated together in order to form the complete zip, since `part_aa` being a zip simply means it holds the zip header.
- **Execution:** Used `cat` to combine all parts into `combined.zip`, then unzipped using the password `supersecret` found in `instructions.txt`.

### 3. Commands Used

```
file part_aa part_ab part_ac part_ad part_ae
cat part_aa part_ab part_ac part_ad part_ae > combined.zip
unzip -P supersecret combined.zip
cat <extracted_file>.txt
```
