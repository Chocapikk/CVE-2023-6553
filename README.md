# CVE-2023-6553 Exploit V2 🚀

## Description 📝

The Backup Migration plugin for WordPress is vulnerable to Remote Code Execution in all versions up to, and including, 1.3.7 via the `/includes/backup-heart.php` file. An attacker can control the values passed to an `include` statement, leveraging that to achieve remote code execution. This vulnerability allows unauthenticated attackers to execute code on the server easily.

## Installation 🛠️

1. Ensure you have Python 3.x installed on your system.

2. Install the required Python libraries by running the following command in your terminal (navigate to the project directory first):

   ```bash
   pip install -r requirements.txt
   ```

## Running the Exploit 🏃

1. After installing the dependencies, you can run the exploit using the following command:

   ```bash
   python exploit.py -u <base_url>
   ```

   Replace `<base_url>` with the base URL of the target WordPress site. Ensure that the target site is vulnerable to CVE-2023-6553 and that you have the appropriate authorization to perform testing.

   For example:

   ```bash
   python exploit.py -u https://example.com
   ```

   The exploit will attempt to exploit the vulnerability and write a PHP file on the target server. You can also specify a list of URLs to check using the `-f` option or output the results to a file using the `-o` option.

2. To use multiple threads for scanning multiple URLs, use the `-t` option followed by the number of threads:

   ```bash
   python exploit.py -f urls.txt -t 10 -o vulnerable.txt
   ```

   This will scan the list of URLs provided in `urls.txt` using 10 threads and output the results to `vulnerable.txt`.

## Using the Interactive Shell 🐚 (if successful)

1. If the exploit successfully writes the PHP file on the target server, you will be given access to an interactive shell to execute commands on the server.

2. The interactive shell operates similarly to a Unix terminal. You can enter commands and see the output.

3. To exit the interactive shell, type `exit`.

4. To clear the screen, type `clear`.

⚠️ Please remember that it is illegal and unethical to use this exploit against systems without explicit permission. Always ensure you have the appropriate authorization before testing the vulnerability of a website.