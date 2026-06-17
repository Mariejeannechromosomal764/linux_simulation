# 🏆 Practice Challenges

Hands-on exercises to use inside the **Cyber Assassins** terminal. Work through them in order — each one builds on the last.

> Open `index.html`, and type the commands directly into the simulator as you read along.

---

## Level 1 — Orientation

1. Find out who you are logged in as.
2. Print your current working directory.
3. List everything in your home folder, including hidden files.
4. Find out what Linux kernel version you're running.

<details>
<summary>Solution</summary>

```bash
whoami
pwd
ls -la
uname -a
```
</details>

---

## Level 2 — File Basics

1. Create a folder called `project`.
2. Inside it, create a file called `notes.txt`.
3. Write the line `Hello Cyber Assassins` into that file.
4. Confirm the content was written correctly.

<details>
<summary>Solution</summary>

```bash
mkdir project
cd project
touch notes.txt
echo "Hello Cyber Assassins" > notes.txt
cat notes.txt
```
</details>

---

## Level 3 — Permissions Puzzle

1. Create a file called `secret.sh`.
2. Try to run it — notice it can't be executed yet.
3. Make it executable for the owner only.
4. Verify the permission change with a long listing.

<details>
<summary>Solution</summary>

```bash
touch secret.sh
ls -la secret.sh
chmod u+x secret.sh
ls -la secret.sh
```
</details>

---

## Level 4 — Become Root

1. Try to enter the `/root` directory as a normal user. What happens?
2. Switch to the root user.
3. Now try entering `/root` again.
4. Return to your normal user account.

<details>
<summary>Solution</summary>

```bash
cd /root        # Permission denied
sudo su         # password: toor
cd /root        # Works now
exit            # back to student
```
</details>

---

## Level 5 — Search & Filter

1. Create three files: `apple.txt`, `banana.txt`, `cherry.txt`.
2. Write the word `fruit` into all three.
3. Use one command to search for the word `fruit` across all `.txt` files in the current folder.
4. Find every file in your home directory ending in `.txt`.

<details>
<summary>Solution</summary>

```bash
echo "fruit" > apple.txt
echo "fruit" > banana.txt
echo "fruit" > cherry.txt
grep "fruit" *.txt
find ~ -name "*.txt"
```
</details>

---

## Level 6 — The Danger Zone (Safe Here!)

1. Try running `rm -rf /` and read what the simulator tells you.
2. Then safely delete just your `project` folder and everything inside it.

<details>
<summary>Solution</summary>

```bash
rm -rf /          # Blocked with an educational warning
cd ~
rm -r project
```
</details>

> ⚠️ **Real-world warning:** On an actual Linux machine, `rm -rf /` would erase your entire operating system. Never run this command for real unless you fully understand what you're doing — and even then, almost never.

---

## Level 7 — Process & System Awareness

1. List all currently running processes in detail.
2. Check how much disk space is used.
3. Check how much memory (RAM) is free.
4. Find the process ID of your current bash shell.

<details>
<summary>Solution</summary>

```bash
ps aux
df -h
free -h
ps aux | grep bash
```
</details>

---

## Level 8 — Networking Fundamentals

1. Check your machine's network interfaces.
2. Ping a host 4 times.
3. Look up the DNS records for a domain.
4. Run a simulated port scan against `localhost`.

<details>
<summary>Solution</summary>

```bash
ifconfig
ping -c 4 google.com
dig google.com
nmap localhost
```
</details>

---

## Level 9 — Text Processing Combo

1. Create a file `numbers.txt` containing: `5`, `2`, `9`, `1`, `2` (one per line).
2. Sort the numbers numerically.
3. Remove duplicate values.
4. Count how many lines are in the final file.

<details>
<summary>Solution</summary>

```bash
echo "5
2
9
1
2" > numbers.txt
sort -n numbers.txt
sort -n numbers.txt | uniq
wc -l numbers.txt
```
</details>

---

## Level 10 — Final Boss: Full Workflow

Simulate a real beginner pentest recon workflow:

1. Create a directory called `recon`.
2. Inside it, run a simulated nmap scan and save a note about the open ports you saw.
3. Use `whois` to check a fictional domain's registration info.
4. Archive the entire `recon` folder into a `.tar.gz` file.
5. Verify the archive was created by listing the directory.

<details>
<summary>Solution</summary>

```bash
mkdir recon
cd recon
nmap target.local
echo "Open ports: 22, 80, 443" > findings.txt
whois target.local
cd ..
tar -czf recon.tar.gz recon/
ls -la
```
</details>

---

## 🎓 What's Next?

Once you're comfortable with everything above:

- Practice on real systems using **TryHackMe** or **HackTheBox** (free tiers available)
- Set up a **Kali Linux VM** using VirtualBox or VMware
- Learn **Bash scripting** to automate the commands you've learned here
- Explore the **man pages** (`man <command>`) for deeper command options

---

Made with ❤️ by Shivam
