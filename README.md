
### Updated **Setup Instructions for the D-TECH Netflix Account Tester**

---

### 1. Update and Upgrade Termux Packages
Update and upgrade Termux packages:

```bash
pkg update && pkg upgrade
```

### 2. Install Required Packages (First Time Only)
Install Python, pip, and unzip utilities:

```bash
pkg install python
pkg install python-pip
pkg install unzip
```

### 3. Download and Move ChromeDriver (First Time Only)

1. **Download ChromeDriver** from the [ChromeDriver download page](https://sites.google.com/chromium.org/driver/) and place it in the Termux `Download` directory.

2. **Move and Extract ChromeDriver**:
   - Navigate to the download directory:

     ```bash
     cd /storage/emulated/0/Download
     ```

   - Extract the `chromedriver-linux64.zip` file:

     ```bash
     unzip chromedriver-linux64.zip
     ```

   - Navigate into the extracted folder:

     ```bash
     cd chromedriver-linux64
     ```

   - Move the `chromedriver` file to Termux’s binary path:

     ```bash
     mv chromedriver /data/data/com.termux/files/usr/bin/
     ```

### 4. Clone the GitHub Repository
Clone the Netflix checker repository from GitHub:

```bash
git clone https://github.com/Preasx24/D-TECH_Netflix_checker.git
```

Navigate into the cloned repository:

```bash
cd D-TECH_Netflix_checker
```

### 5. Create and Edit `requirements.txt` (First Time Only)

1. Create the `requirements.txt` file:

   ```bash
   nano requirements.txt
   ```

2. Add the following dependencies:

   ```
   requests
   beautifulsoup4
   colorama
   selenium
   ```

3. Save and exit:
   - Press `CTRL + X`.
   - Press `Y` to confirm.
   - Press `ENTER` to confirm the filename.

### 6. Install Python Packages
Install the dependencies listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```

### 7. Add Accounts to `netflix` File

1. **Open the `netflix` file for editing**:

   ```bash
   nano netflix
   ```

2. **Add the Netflix account details**:
   Add each account detail (such as email and password) in the format expected by the script. For example:

   ```
   example1@gmail.com:password1
   example2@gmail.com:password2
   ```

3. **Save the file**:
   - Press `CTRL + X` to exit the editor.
   - Press `Y` to confirm saving changes.
   - Press `ENTER` to confirm the filename.

### 8. Run the Script
After setting up the accounts, you can run the script:

```bash
python D-TECH_Netflix_checker.py
```

---