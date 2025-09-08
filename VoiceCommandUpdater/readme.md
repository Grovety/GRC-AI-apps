# VoiceCommandUpdater  

This application is designed for **voice command recognition** and their **dynamic updating**.  
It allows users to **easily configure and refresh commands** recognized by the device **without changing the code or reflashing the core firmware**.  

The main goal is to show that the end user can modify the set of recognized voice commands on their own and instantly use them — for example, to control a CrowBot robot.  

---

## ⚙️ What’s New in This Version  

- Support for **two recognition languages**: English (EN) and Chinese in pinyin format (CN).  
- Implemented **language switching via voice phrases** (system/reserved phrases).  
- Added recommended command file formats for EN and CN.  
- A new CrowBot firmware has been added to the repository  
  [Bolt_grc_program.ino](https://github.com/Grovety/CrowBot_GRC_program/blob/main/Bolt_grc_program.ino)  
  with command handler templates, so users can test the functionality “out of the box.”  

---

## ⚙️ Installation & Launch  

### 1. Initial Board Flashing (DevBoard / GRC AI Robot Control)  
1. Connect the board to your PC via the **left USB-C (labeled ESP32-S3)**.  
   This port is used for the **initial flashing** of the device.  
2. Run **`flash_tool_s3.exe`** and flash the VoiceControl image.  
   Wait until the process completes successfully.  

---

### 2. UART Connection for Command Updates  
1. Connect the **second USB-C (labeled UART)** — this port is used to upload `commands` into SPIFFS.  
2. Open **`update_commands.exe`**. The program will automatically try to detect the COM port.  
   Typically, it appears as *“Silicon Labs CP210x USB to UART Bridge”*.  
   If the port is not detected, the utility will prompt you to select it manually.  

> ⚠️ **Tip:** If the port is not detected, install the **CP210x driver** (Silicon Labs) and make sure the port is not being used by other applications.  

---

### 3. Working with Commands (add/remove/edit)  
1. The project folder contains the command files. It is recommended to use two separate files:  
   - `commands_en.txt` — English commands (EN).  
   - `commands_cn.txt` — Chinese commands in pinyin (CN).  
2. Edit the appropriate file in any text editor (e.g., VSCode, Notepad++).  
   - **EN:** one command per line, uppercase letters (UPPERCASE).  
   - **CN:** one phrase per line, lowercase letters, words separated by spaces (pinyin).  
3. Save the file with **UTF-8 encoding (without BOM)**.  
4. Place the file(s) next to `update_commands.exe` and run the utility.  
   It will pack and write the commands into SPIFFS via UART.  
5. After completion, reboot the DevBoard (if the utility hasn’t done so automatically).  
   The new user-defined commands will now be available for recognition.  

> ⚠️ **Note:** The board contains a built-in factory set of system commands that cannot be removed by the user.  
> You can only add, edit, or delete your own custom entries.  

---

## 📝 Command Format — Examples  

**Example `commands_en.txt`**  
```txt
GO FORWARD
TURN LEFT
STOP
PLAY MUSIC
DANCE TANGO
