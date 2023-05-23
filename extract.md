```python
import zipfile
import os

def unzip_files(zip_dir, extract_dir):
    # Check if the extraction directory exists, if not, create it
    if not os.path.exists(extract_dir):
        os.makedirs(extract_dir)

    # Iterate over all files in the specified directory
    for file_name in os.listdir(zip_dir):
        if file_name.endswith('.zip'):
            file_path = os.path.join(zip_dir, file_name)

            # Open the ZIP file
            with zipfile.ZipFile(file_path, 'r') as zip_ref:
                # Extract all files to the specified directory
                zip_ref.extractall(extract_dir)

            print(f"Extracted: {file_name}")

# Provide the directory containing the ZIP files
zip_directory = r'C:\Users\Dipes\Downloads\A'

# Provide the directory where the files should be extracted
extract_directory = r'C:\Users\Dipes\Downloads\A1'

# Call the unzip_files function
unzip_files(zip_directory, extract_directory)

```

    Extracted: 20048805AAYUSHKHANAL_94222.zip
    Extracted: 20049383Ashutoshkhadka_91096.zip
    Extracted: 21039798AavaThapa2_75db50d3-c5d8-4c1b-992c-a55525551fd9_90639_.zip
    Extracted: 21039801AayushaLamichhane_90689.zip
    Extracted: 21049464_AashutoshSanjel_90950.zip
    Extracted: 21049465_AaurasKoirala_90756.zip
    Extracted: 21049466AavashTamrakar_90896.zip
    Extracted: 21049467AayamMaharjan_91088.zip
    Extracted: 22015635AAVASHHAMAL_91031.zip
    


```python

```
