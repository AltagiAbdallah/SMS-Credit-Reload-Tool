# SMS Credit Reload Tool

A finance portal widget designed for **MikeTango** to streamline SMS credit top-ups for their clients. This tool allows Finance Executives to select brands, handle complex multi-company invoicing, and generate quotations via a simulated Quickbooks integration.

🔗 **Live Demo:** [View Deployed App](https://698c4ca89a49bebc22065d33--mellifluous-sherbet-11fdbc.netlify.app/)

## 📋 Features

* **Dynamic Brand Selection:** Select a client brand to load their specific outlet structure.
* **Multi-Company Logic:** Handles complex scenarios where outlets under the same brand belong to different Legal Entities (Sdn Bhd).
* **Real-Time Calculation:** Automatically updates the total top-up amount as users input credits.
* **Validation:** Prevents submission of zero-value or empty orders.
* **Simulated Workflow:** Mimics the API latency and success states for Quickbooks quotation generation and email triggers.

## 🛠️ Tech Stack

* **HTML5**
* **Tailwind CSS** (via CDN for styling)
* **Vanilla JavaScript** (DOM manipulation & Logic)

## 🚀 How to Run Locally

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/SMS-Credit-Reload-Tool.git](https://github.com/your-username/SMS-Credit-Reload-Tool.git)
    ```
2.  **Navigate to the project folder:**
    ```bash
    cd SMS-Credit-Reload-Tool
    ```
3.  **Open `index.html`:**
    You can double-click the file to open it in your browser, or use a live server extension in VS Code.

## 🧪 Testing Scenarios

Use the following data to test the business logic implemented in the tool:

### Scenario A: Multi-Company Mapping (Critical)
* **Select Brand:** `Silvertree Restaurants`
* **Observation:** You will see "Binjai Park" listed three times. This is intentional.
    * Row 1: *Silvertree Oris Sdn Bhd*
    * Row 2: *Silvertree Binjai Sdn Bhd*
    * Row 3: *Silvertree Benja Sdn Bhd*
* **Action:** Enter `300` for each.
* **Result:** Total should equal `900`.

### Scenario B: Zero Value Validation
* **Select Brand:** Any (e.g., `Gordon Grill`)
* **Action:** Leave all fields at `0` or empty.
* **Attempt:** Click "Next".
* **Result:** The system should alert "Please enter a top-up amount greater than 0" and prevent submission.

## 📂 Project Structure

```text
SMS-Credit-Reload-Tool/
├── index.html       # The main application file (contains HTML, CSS, & JS)
├── README.md        # Project documentation
└── assets/          # (Optional) Images or static files
