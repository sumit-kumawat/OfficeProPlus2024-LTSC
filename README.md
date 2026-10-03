# Office LTSC Professional Plus 2024 — Offline Installation

This folder contains the downloaded installation files for **Microsoft Office LTSC Professional Plus 2024 (64-bit, English)**.

## Folder Structure

```text
office2024/
├── setup.exe
├── configuration.xml
├── Download-Office2024.bat
└── Office/
    └── Data/
        └── 16.0.17932.21000/
```

## System

* **Product:** Microsoft Office LTSC Professional Plus 2024
* **Architecture:** 64-bit
* **Language:** English (`en-us`)
* **Channel:** `PerpetualVL2024`
* **Product ID:** `ProPlus2024Volume`
* **Installation type:** Offline

---

## Installation

### 1. Open Command Prompt as Administrator

1. Open the Windows **Start** menu.
2. Type `CMD`.
3. Right-click **Command Prompt**.
4. Select **Run as administrator**.
5. Click **Yes** if Windows asks for permission.

### 2. Go to the Office folder

Run:

```cmd
cd /d "C:\Users\Administrator\Downloads\office2024"
```

You should now see:

```text
C:\Users\Administrator\Downloads\office2024>
```

### 3. Start the offline installation

Run:

```cmd
setup.exe /configure configuration.xml
```

Press **Enter**.

The installer will use the Office files already downloaded in the `Office` folder.

---

## Verify Installation

After installation, open **Microsoft Word**.

Go to:

**File → Account**

Under **Product Information**, verify that the installed product is:

```text
Microsoft Office LTSC Professional Plus 2024
```

You can also start Word directly from Command Prompt:

```cmd
"C:\Program Files\Microsoft Office\root\Office16\WINWORD.EXE"
```

---

## Check Office Version

To check the installed Office version:

1. Open **Word**.
2. Select **File**.
3. Select **Account**.
4. Select **About Word**.

The About window displays the installed Office version and build number.

---

## Offline Installation

The Office installation files have already been downloaded.

The offline package is located under:

```text
Office\Data\
```

For example:

```text
Office\Data\16.0.17932.21000
```

After the download is complete, the installation command is:

```cmd
setup.exe /configure configuration.xml
```

No second Office package download is required for this installation.

---

## Activation

Installation and activation are separate.

This package installs the Office LTSC software. Activation requires a **legitimate Office LTSC 2024 volume license**, such as:

* MAK activation
* Organization's KMS activation

Use the activation method provided by your organization or Microsoft licensing agreement.

Do not use unauthorized activators or modified Office files.

---

## Troubleshooting

### `setup.exe` is not recognized

Make sure Command Prompt is in the correct folder:

```cmd
cd /d "C:\Users\Administrator\Downloads\office2024"
```

Then run:

```cmd
setup.exe /configure configuration.xml
```

### Installation does not start

Verify that these files exist:

```text
setup.exe
configuration.xml
Office\Data\
```

Run:

```cmd
dir
```

### Check the configuration

Run:

```cmd
type configuration.xml
```

The configuration should contain:

```xml
<Configuration>
  <Add OfficeClientEdition="64" Channel="PerpetualVL2024">
    <Product ID="ProPlus2024Volume">
      <Language ID="en-us" />
    </Product>
  </Add>
  <RemoveMSI />
  <Display Level="None" AcceptEULA="TRUE" />
</Configuration>
```

---

## Quick Install

For a previously downloaded package, run these commands from **Command Prompt as Administrator**:

```cmd
cd /d "C:\Users\Administrator\Downloads\office2024"
setup.exe /configure configuration.xml
```

---

## Microsoft Documentation

For official deployment information, see:

* Microsoft Office Deployment Tool
* Microsoft Office LTSC 2024 deployment documentation

Use Microsoft's official documentation for licensing, deployment, configuration, and troubleshooting information.

---

**Package:** Office LTSC Professional Plus 2024
**Architecture:** x64
**Language:** English
**Installation:** Offline
**Status:** Installation files downloaded
