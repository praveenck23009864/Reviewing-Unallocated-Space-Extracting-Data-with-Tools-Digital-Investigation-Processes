## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
<img width="1920" height="1080" alt="Screenshot 2025-09-22 105035" src="https://github.com/user-attachments/assets/a3b68d9d-e4c4-4a47-8931-a8b6c755acaa" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 105035" src="https://github.com/user-attachments/assets/f4d03e5f-3b3a-4cf8-b9ee-66ae6e56038d" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 103231" src="https://github.com/user-attachments/assets/00819071-d52a-4c30-b281-7df57d811b25" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 103254" src="https://github.com/user-attachments/assets/0a6f33bd-660a-407b-a402-51f624e901f1" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 103434" src="https://github.com/user-attachments/assets/31529871-178d-4398-ae72-c26f7056f4db" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 105259" src="https://github.com/user-attachments/assets/fb7f131d-2d69-4cc9-a0ff-b9292cc5f66f" />



Unallocated Space Analysis and Extracted Data Report

## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

