# Project 03 - Google Cloud Storage Backup & Restore

## 📖 Overview

This project demonstrates how to build a simple backup and recovery solution using **Google Cloud Storage**.

A structured backup directory was created locally, uploaded to a Cloud Storage bucket, and successfully restored to verify that the backup process worked correctly.

This project simulates how organizations protect important files and recover them when needed.

---

## 🎯 Project Objectives

- Create a Cloud Storage backup bucket
- Organize backup files into folders
- Upload backups using Cloud Shell
- Verify uploaded files
- Restore backups from Cloud Storage
- Validate the recovery process

---

## ☁️ Google Cloud Services Used

- Google Cloud Storage
- Google Cloud Shell
- Google Cloud CLI (`gcloud storage`)

---

## 🏗️ Architecture

```text
Local Backup Files
        │
        ▼
Google Cloud Shell
        │
        ▼
Google Cloud Storage Bucket
        │
        ▼
Backup Stored Securely
        │
        ▼
Restore Files
```

---

## 📂 Project Structure

```text
backups/
├── documents/
│   └── student_records.txt
├── website/
│   └── index.html
└── images/
    └── logo.txt
```

---

## ⚙️ Steps Performed

1. Created a Google Cloud Storage bucket.
2. Created a structured backup directory.
3. Generated sample backup files.
4. Uploaded the entire directory using recursive copy.
5. Verified uploaded files.
6. Restored the backup to a local directory.
7. Verified the restored files.

---

## 💻 Key Commands

Create bucket

```bash
gcloud storage buckets create gs://$BACKUP_BUCKET --location=US
```

Upload backup

```bash
gcloud storage cp --recursive backups gs://$BACKUP_BUCKET
```

Verify backup

```bash
gcloud storage ls --recursive gs://$BACKUP_BUCKET
```

Restore backup

```bash
gcloud storage cp --recursive gs://$BACKUP_BUCKET/backups restored-files
```

---

## 📸 Screenshots

- Bucket created
- Cloud Shell commands
- Backup verification
- Restore verification

(Add screenshots to the `screenshots` folder.)

---

## 🌍 Real-World Use Cases

Organizations use cloud backups to:

- Protect business data
- Recover files after accidental deletion
- Support disaster recovery
- Store long-term archives
- Meet compliance and regulatory requirements

---

## 📚 Lessons Learned

Through this project I learned how to:

- Create Cloud Storage buckets
- Organize backup data
- Upload directories recursively
- Verify uploaded files
- Restore backups successfully
- Understand why backup verification is essential

---

## 🚀 Future Improvements

- Enable Object Versioning
- Configure Lifecycle Management
- Encrypt sensitive backup data
- Automate backups using Cloud Scheduler
- Use Archive Storage for long-term retention

---

## 👨‍💻 Author

**Caleb Attah**

Aspiring Google Cloud Engineer & Cloud Architect

GitHub:
https://github.com/ProfKay230
