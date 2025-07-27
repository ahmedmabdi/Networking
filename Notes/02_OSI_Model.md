# 02 - OSI Model & TCP/IP Model

## 📚 What is the OSI Model?

- OSI = **Open Systems Interconnection** Model.
- A conceptual framework to understand how data flows through a network.
- Divides networking into **7 layers**, each with specific responsibilities.
- Helps standardize network functions across hardware/software vendors.

---

## 🧱 The 7 Layers of OSI Model (Bottom to Top)

| Layer | Name              | Function |
|-------|-------------------|----------|
| 7     | Application        | Interfaces with end-user apps (HTTP, FTP, DNS). |
| 6     | Presentation       | Formats/translates data (e.g., encryption, compression, encoding). |
| 5     | Session            | Manages sessions between applications. |
| 4     | Transport          | Reliable delivery, error handling (TCP/UDP). |
| 3     | Network            | Routing, IP addressing (IPv4/IPv6). |
| 2     | Data Link          | MAC addresses, switching, error detection. |
| 1     | Physical           | Cables, signals, hardware — actual transmission of bits. |

---

## 🧭 Importance of Each Layer

- **Layer 1 (Physical):** Converts digital data into electrical/optical signals.
- **Layer 2 (Data Link):** Ensures data frames are sent to the correct device.
- **Layer 3 (Network):** Moves data across networks using IP addresses.
- **Layer 4 (Transport):** Handles delivery (TCP = reliable, UDP = fast).
- **Layer 5 (Session):** Maintains communication between devices (login/logout).
- **Layer 6 (Presentation):** Encrypts/decrypts, compresses data.
- **Layer 7 (Application):** Provides network services to users.

---

## 🔁 Sender vs. Receiver POV

- **Sender:** Data flows **top to bottom** through the layers (App → Physical).
- **Receiver:** Data flows **bottom to top** (Physical → App).

---

## 🌐 TCP/IP Model (Used in Real-World)

| TCP/IP Layer | Corresponding OSI Layers        | Functions |
|--------------|----------------------------------|-----------|
| Application  | OSI Layers 5, 6, 7               | Web, Email, FTP |
| Transport    | OSI Layer 4                      | TCP, UDP |
| Internet     | OSI Layer 3                      | IP addressing, routing |
| Network Access | OSI Layers 1 & 2               | Physical & MAC-level transmission |

📝 **Note:** TCP/IP is simpler (4 layers) and widely implemented today.
