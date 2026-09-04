# 🐧 Bandit Linux Journey – Day 1

Platform: [OverTheWire Bandit](https://overthewire.org/wargames/bandit/bandit1.html)

---

## Level 0 → 1
**Task:** Password stored in `readme` file in home directory.  
**Steps:**
1. `ssh bandit0@bandit.labs.overthewire.org -p 2220`
2. Enter password: `bandit0`
3. `ls`
4. `cat readme`

**Problem faced:** None ✅

---

## Level 1 → 2
**Task:** Password stored in file named `-`.  
**Steps:**
1. Login with previous password
2. `ls`
3. `cat ./-`

**Problem faced:** Didn’t know how to handle special filename `-`. Learned to use `./`.

---

## Level 2 → 3
**Task:** Password stored in file with spaces in its name.  
**Steps:**
1. `ls`
2. `cat "spaces in this filename"`

**Problem faced:** Needed quotes to handle spaces. Learned `--` avoids confusion with commands.

---

## Level 3 → 4
**Task:** Password stored in hidden file inside `inhere`.  
**Steps:**
1. `ls -l` (shows non-hidden files)
2. `ls -la` (shows hidden files)
3. `cd inhere`
4. `cat .hidden`

**Problem faced:** Learned `-a` shows hidden files.

---

## Level 4 → 5
**Task:** Password stored in only human-readable file inside `inhere`.  
**Steps:**
1. `ls -la`
2. `cd inhere`
3. `file ./*`
4. `cat <filename>`

**Problem faced:** Learned `*` expands to all files in current directory.

---

### 🔑 Key Takeaways
- `ssh` → remote login  
- `ls -a` / `ls -la` → list hidden files  
- `cat` → read file contents  
- `file` → identify file type  
- Quoting & escaping → handle tricky filenames  

---

📓 **Reflection:** Today I learned how to deal with special filenames (`-`, spaces), hidden files, and wildcards. These are basic but powerful skills for cybersecurity and forensic analysis.
