
# **GitRaider**  
_A tool to mass hunt exposed `.git` directories on websites._

## **Overview**
GitRaider is a powerful and automated tool written in Go, designed to identify exposed `.git` directories on web servers. 
Exposing `.git` directories can lead to the disclosure of sensitive information, including source code, credentials, and 
configuration files. GitRaider helps developers, penetration testers, and security professionals identify and remediate such risks effectively.

## **Features**
- Fast and efficient scanning powered by Go’s concurrency model.
- Automated detection of exposed `.git` directories.
- Output results in a structured format (JSON, CSV, etc.).
- Supports bulk domain input via files.
- Simple CLI interface.

## **Use Cases**
1. **Penetration Testing:** Quickly locate vulnerable `.git` directories during security assessments.
2. **Bug Bounty Hunting:** Identify and report exposed `.git` directories to bug bounty programs.
3. **Self-Auditing:** Scan your own assets to ensure `.git` directories are not publicly accessible.

## **Installation**
### Prerequisites
- Go 1.19+

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/brianokinyi/GitRaider.git
   cd GitRaider
   ```
2. Build the binary:
   ```bash
   go build -o gitraider main.go
   ```

## **Usage**
### Basic Usage
Scan a single URL:
```bash
./gitraider --url https://example.com
```

### Bulk Scan
Scan multiple URLs from a file:
```bash
./gitraider --input urls.txt
```

### Output Options
Save results in JSON format:
```bash
./gitraider --url https://example.com --output results.json
```

### Help Menu
Access the full list of options:
```bash
./gitraider --help
```

## **Output Example**
```json
{
  "url": "https://example.com",
  "status": "vulnerable",
  "files": [
    ".git/config",
    ".git/HEAD"
  ]
}
```

## **Contributing**
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a detailed description.

## **License**
This project is licensed under the [MIT License](LICENSE).

## **Disclaimer**
This tool is for educational and ethical testing purposes only. Misuse of this tool is prohibited and may lead to legal consequences.
