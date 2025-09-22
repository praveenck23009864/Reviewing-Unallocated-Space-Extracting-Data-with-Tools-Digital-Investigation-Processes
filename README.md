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
<img width="1920" height="1080" alt="Screenshot 2025-09-22 105035" src="https://github.com/user-attachments/assets/10eccbc0-b371-4e7f-92ed-65efd72630ae" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 105157" src="https://github.com/user-attachments/assets/f49a570b-c6c8-43d6-bef3-4c7204886c85" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 103254" src="https://github.com/user-attachments/assets/a05b2705-ae2a-47b2-97c6-93950803297d" />
+<img width="1919" height="1076" alt="Screenshot 2025-09-22 103337" src="https://github.com/user-attachments/assets/e8a4a6c8-dc0c-44bb-89b9-acb8f90c6381" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 103434" src="https://github.com/user-attachments/assets/647debe6-b12d-40df-937b-fedec7612f32" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 103434" src="https://github.com/user-attachments/assets/a79a9ed8-11e9-467e-8cb5-8d7cc85a9676" />
<img width="1920" height="1080" alt="Screenshot 2025-09-22 105259" src="https://github.com/user-attachments/assets/bac90aaa-4596-45c8-ab2b-32cf84ccd50b" />




## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

