# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details
<img width="1600" height="899" alt="69491951-37ac-4c66-b518-61e1a7383ab5" src="https://github.com/user-attachments/assets/473a6e86-a608-424a-9023-681ee01d3240" />
<img width="1600" height="899" alt="724aab7d-d4e5-4927-9f79-ec89aa9ee636" src="https://github.com/user-attachments/assets/fd14a050-b431-4aaa-8439-599c55058f65" />
<img width="1600" height="898" alt="fca8dbec-b34f-4484-8766-ee5fdf63a8d0" src="https://github.com/user-attachments/assets/078870f1-6d5b-4408-be96-92ccc7c6a1fd" />
<img width="1600" height="898" alt="813d55a0-d079-4f99-84d7-8a3023f7d6a9" src="https://github.com/user-attachments/assets/98619daf-830e-4063-b783-92d87da55579" />
<img width="1600" height="899" alt="4e29fc60-5b68-4617-af89-ae14faf07a46" src="https://github.com/user-attachments/assets/508326c9-be82-4a9b-b5b3-4e773933e9cf" />
<img width="1600" height="899" alt="e2a04c9b-69f8-4fa6-9f44-aac867d12f19" src="https://github.com/user-attachments/assets/7cdda724-4082-461a-a895-82d8a04db0be" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
