# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
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
Unallocated Space Analysis and Extracted Data Report
<img width="1920" height="1080" alt="Screenshot 2025-09-20 160354" src="https://github.com/user-attachments/assets/71ad99b6-8462-494d-8ff0-e3da020c7ec5" />
<img width="1920" height="1080" alt="Screenshot 2025-09-20 160423" src="https://github.com/user-attachments/assets/b1c02813-fa77-47a9-9be1-ba97ff0dba88" />
<img width="1920" height="1080" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/6df7e55c-292a-4d9c-8151-68a2e82be74e" />
<img width="1920" height="1080" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/01efea70-9a1e-4d37-a2f3-6f3f766a230e" />

<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/cebb83ba-8e16-4bf9-8bf5-82feb15e5254" />
## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

