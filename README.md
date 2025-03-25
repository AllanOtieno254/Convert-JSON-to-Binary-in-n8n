#  Convert JSON to Binary in n8n 

## **Overview**  
This n8n workflow fetches random poetry data from the **Poetry DB API**, converts the JSON response into a binary file, writes the file to disk, and then reads it back to verify the process.  
![main workflow ](https://github.com/user-attachments/assets/f290c7ea-4430-4f5b-aa8e-d853ebf3ff61)

## **Workflow Steps**  

1. **Trigger the workflow**  
   - The workflow starts when the **"Test Workflow"** button is clicked.  

2. **Make an HTTP request**  
   - The **HTTP Request** node fetches random poetry data from [PoetryDB](https://poetrydb.org/random/1).  

3. **Convert JSON to Binary**  
   - The **Convert to File** node transforms the JSON response into a binary file.  

4. **Write Binary Data to Disk**  
   - The **Read/Write Files from Disk** node saves the binary file to the local machine.  

5. **Read the Binary File**  
   - Another **Read/Write Files from Disk** node retrieves and reads the binary file to confirm that the process was successful.  

## **Requirements**  
- n8n installed and running on your machine.  
- Internet access to fetch data from PoetryDB.  

## **Expected Outcome**  
After execution, a binary file containing the poetry JSON data should be created and successfully read back from the disk.  

## **Notes**  
- If the workflow stops due to **"No output data returned,"** enable **Always Output Data** in the node settings.  
- Ensure the correct file path is used when writing and reading the file.  

---
