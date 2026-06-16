
# 📄 Direct PDF Extractor & Downloader

Welcome! This is a complete step-by-step guide to extract and download PDFs from restricted document viewers. 

**You do not need any coding knowledge to use this.** Just follow these simple steps in order.

---

## 🛠️ Complete Step-by-Step Process

### Step 1: Block JavaScript & Open Developer Tools
1. Open the website where your PDF is located.
2. Click on the **Padlock icon (🔒)** or **Site Settings icon** next to the website address.
3. Find **JavaScript** and change it to **Block**, then reload the page.
4. Right-click anywhere on the page and select **Inspect** (or press `Ctrl + Shift + I`).
5. Click on the **Network** tab inside the Inspect panel.

### Step 2: Find and Copy the Hidden Viewer Link
1. Now, click on the button to open the PDF on the website.
2. Look at the **Network** tab. You will see a list of files loading.
3. Click on the very first file at the top (under the "Document" type).
4. On the right side, find the **Headers** tab, and look under the **General** section.
5. Copy the **Request URL** you see there.
6. Open a **New Tab** in your browser and paste this copied URL to open it.

### Step 3: Open the Console
1. On this new tab, right-click anywhere and select **Inspect** again.
2. This time, click on the **Console** tab.
3. You will see a blank space where you can type or paste text.

### Step 4: Extract the Direct PDF Link
Copy the code below, paste it into the **Console**, and press **Enter**. This will show you the direct, unblocked URL of the PDF.

```javascript
new URL(location.href).searchParams.get("file")

```

### Step 5: Open the PDF in a Clean New Tab

Next, copy the code below, paste it into the **Console**, and press **Enter**. This will automatically open your extracted PDF in a fresh, clean tab without any viewer restrictions.

```javascript
window.open(
  new URL(location.href).searchParams.get("file"),
  "_blank"
)

```

### Step 6: Force Download the PDF to Your Device

Finally, to save the PDF directly to your computer or phone, copy the code below, paste it into the **Console**, and press **Enter**. The file will start downloading immediately.

```javascript
const a = document.createElement("a");
a.href = new URL(location.href).searchParams.get("file");
a.download = "Downloaded_Document.pdf";
a.click();

```

---

## ✅ Success!

By following these steps, you have successfully:

* Bypassed the viewer restrictions.
* Found the hidden PDF URL.
* Opened the PDF properly.
* Downloaded the file safely to your device.

```

```
