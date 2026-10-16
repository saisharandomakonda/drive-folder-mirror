# Full Drive Mirror Archive

All downloaded files from the Google Drive folder are packaged in `drive-full-mirror.tar.gz.b64` (split into two parts for upload).

## How to restore the files

1. Download both parts from this repo:
   - `drive-full-mirror.part1.b64`
   - `drive-full-mirror.part2.b64`

2. Combine them:
   ```bash
   cat drive-full-mirror.part1.b64 drive-full-mirror.part2.b64 > drive-full-mirror.tar.gz.b64
   ```

3. Decode:
   ```bash
   base64 -d drive-full-mirror.tar.gz.b64 > drive-full-mirror.tar.gz
   ```

4. Extract:
   ```bash
   tar -xzf drive-full-mirror.tar.gz
   ```

You will get the full folder structure with all Job Description.txt files and Resume.docx / Resume.pdf files that were successfully downloaded.

This contains everything I was able to pull from the Drive folder.