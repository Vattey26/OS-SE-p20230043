# Lab 1 Submission
- **Name :** HEN Chhorda Vattey
- **ID :** p20230043

---

## Task 1: Operating System Identification

```
uname -a > task1_os_info.txt
lsb_release -a 2>/dev/null >> task1_os_info.txt
lsb_release -a 2>/dev/null >> task1_os_info.txt
```

<img width="1525" height="186" alt="image" src="https://github.com/user-attachments/assets/c2df4929-7813-433e-a300-0af323b599d9" />

## Task 2: Essential Linux File and DIrectory Commands

```
pwd > ../task2_file_commands.txt
ls >> ../task2_file_commands.txt
touch a.txt b.txt
ls >> ../task2_file_commands.txt
echo "This is file A" > a.txt
echo "This is file B" > b.txt
cat a.txt b.txt >> ../task2_file_commands.txt
cp a.txt a_copy.txt
ls >> ../task2_file_commands.txt
mv b.txt b_renamed.txt
ls >> ../task2_file_commands.txt
rm a_copy.txt
ls >> ../task2_file_commands.txt
```

<img width="1669" height="486" alt="image" src="https://github.com/user-attachments/assets/fadb953a-4550-49d2-a04b-9df784ec44de" />

## Task 3: Package Management Using APT

```
sudo apt-get update > task3_apt_update.txt
sudo apt-get install mc -y > task3_apt_install.txt
which mc > task3_verify_install.txt
ls -ld /etc/mc >> task3_verify_install.txt
sudo apt-get remove mc -y > task3_apt_remove.txt
ls -ld /etc/mc > task3_config_after_remove.txt
sudo apt-get purge mc -y > task3_apt_purge.txt
ls -ld /etc/mc > task3_config_after_purge.txt 2>&1
```

<img width="1565" height="276" alt="image" src="https://github.com/user-attachments/assets/f79afe57-2122-46f3-ae7f-fae8668dc40e" />

## Task 4: Programs vs Processes (Single Process)

```
sleep 120 &
ps > task4_process_list.txt
```

<img width="1222" height="97" alt="image" src="https://github.com/user-attachments/assets/b5d0991c-25c6-4383-8b81-83ad1930f91b" />

## Task 5: Installing Real Applications & Observing Multitasking

```
sudo apt-get install htop tmux -y
which htop tmux > task5_app_verify.txt
sleep 500 &
sleep 600 &
python3 -m http.server 8080 &
ps > task5_multitasking.txt
```
<img width="2539" height="1461" alt="image" src="https://github.com/user-attachments/assets/79dcd25f-d67b-43e2-91f0-469d2eb0204e" />

## Task 6: Virtualization and Hypervisor Detection

```
systemd-detect-virt > task6_virtualization_check.txt
lscpu | grep -i hypervisor >> task6_virtualization_check.txt
uname -r >> task6_virtualization_check.txt
hostname >> task6_virtualization_check.txt
```
<img width="1246" height="276" alt="image" src="https://github.com/user-attachments/assets/eec41e60-a73e-4b1a-b9c8-6fcd8113cdfe" />

---

## Repository and file structure

```
.
├── task1_os_info.txt
├── task2_file_commands.txt
├── task2_files
│   ├── a.txt
│   └── b_renamed.txt
├── task3_apt_install.txt
├── task3_apt_purge.txt
├── task3_apt_remove.txt
├── task3_apt_update.txt
├── task3_config_after_purge.txt
├── task3_verify_install.txt
├── task4_process_list.txt
├── task5_app_verify.txt
├── task5_multitasking.txt
└── task6_virtualization_check.txt
```
