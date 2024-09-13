
## Setup Instructions for the D-TECH NETFLIX ACCOUNT TESTER for Termux

### 1. Update and Upgrade Termux Packages

```bash
pkg update && pkg upgrade
```

### 2. Install Required Packages

```bash
pkg install python
pkg install python-pip
pkg install unzip
```

### 3. Download ChromeDriver

1. **Find the ChromeDriver version that matches your Chrome version** by visiting [ChromeDriver download page](https://chromedriver.chromium.org/downloads).

2. **Download ChromeDriver** from your external app and place it in the Termux download directory.

3. **Move and Extract ChromeDriver**:

   - Navigate to the directory where the downloaded file is located:
     ```bash
     cd /storage/emulated/0/Download
     ```

   - Extract the file:
     ```bash
     unzip chromedriver_linux64.zip
     ```

   - Move the `chromedriver` file to a directory in your PATH (e.g., `/data/data/com.termux/files/usr/bin/`):
     ```bash
     mv chromedriver /data/data/com.termux/files/usr/bin/
     ```

### 4. Create and Edit `requirements.txt`

1. **Create `requirements.txt`**:

   ```bash
   nano requirements.txt
   ```

2. **Add the following dependencies**:

   ```
   requests
   beautifulsoup4
   colorama
   selenium
   ```

3. **Save and Exit**:
   - Press `CTRL + X` to exit.
   - Press `Y` to confirm changes.

### 5. Install Python Packages

```bash
pip install -r requirements.txt
```

### 6. Run the Script

```bash
python D-TECH_Netflix_checker.py
```
