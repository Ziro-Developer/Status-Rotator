## 🌀 Discord Status Rotator

A lightweight selfbot script that cycles through custom status messages on Discord. Built using `discord.py-self`, this tool allows you to update your presence in real time using a selfbot token. All statuses are managed via a simple `config.json` file.

---

### ✨ Features

* Automatically rotates status messages in a loop
* Fully customizable status list
* Quick and easy setup

---

### 🔧 Requirements

* Python 3.10 or higher
* Libraries:

  * `discord.py-self`
  * `colorama` (for colorful terminal output)

---

### 📦 Installation

1. **Clone the repository** or download the source files.

2. **Install the required Python packages**:

   ```bash
   pip install discord
   pip install discord.py-self
   pip install colorama
   ```

   Or, install everything using the `requirements.txt` file:

   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your configuration** by creating a `config.json` file in the root directory:

   ```json
   {
       "statuses": [
           "💻 Running code (Aizer)",
           "🌐 Connecting to server (Aizer)",
           "🛠 Maintenance mode (Aizer)"
       ],
       "rtsec": 2,
       "Token": [""]
   }
   ```

   * `Token`: Your selfbot Discord token
   * `statuses`: A list of statuses that the script will rotate through
   * `rtsec`: Delay in seconds between each status update

4. **Run the script**:

   ```bash
   python status.py
   ```

---

### ▶ How It Works

Once launched, the bot continuously updates your Discord status based on the messages in the config. The rotation interval is controlled by the `rtsec` value.

