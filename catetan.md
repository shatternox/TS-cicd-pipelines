# Sesi 1 - 24 Juni 2021

## Building CI/CD Pipelines with Jenkikns
>>> Muhammad Sidiq Putra - Development Operations (DevOPS) Lead at tiket.com

Problem before devops
- Developer hanya menyentuh pembuatan aplikasinya, tetapi sekalinya deployment semuanya diserahkan ke team deployment.
- Developer langsung lepas tangan dan semuanya dilempar ke team sysadmin/infra, dilempar.
- Team Infra deploy secara manual. Kadang yang di deploy sysadmin tidak berjalan sesuai dengan yang di environment developer ketika dijalankan.
"Di local gw jalan! Salah lu kali deploynya"

- Sekarang sudah diintegrasi dengan DevOPS jadi menghilangkan masalah tersebut.
- Masalahnya apa sih? Version di local dia sama yang ada di tim OPS beda, Knowledge terhadap aplikasinya beda, Environmentnya berbeda.

1. What is DevOPS
- Praktek, praktisi, atau pendekatan untuk mengautomatisasi dan mengintegrasi antara proses development (software engineering) dan IT operation (deployment).
- Harus punya knowledge tentang software lifecycle dan lots of infrastructure/sysadmin stuff.

2. CI/CD Introduction
- Continuous Integration >>> automasi build process, unit test, integration test, quality gate, security check.
- Continuous Deployment >>> automasi release dan deploy setiap ada update. Tapi tentu ada triggernya, harus dicek updatenya bener apa kgk. Pastikan jgn broken.

3. Why we need CI/CD
Continuous Intgration:
- Detects errors as quickly as possible 
    - Fix while fresh in your mind
- Reduces Integration Problem
    - Masalahnya masih kecil, udah ketauan problemnya, semakin mudah dibenerin. Kalo dah terlanjur deploy, jadi susah cari errornya, cari rootcause errornya.
- Allows teams to develop faster, with more confidence

Continous Delivery:
- Ensures that every chane to the system is releasable.
- Lowers risk of each release - makes releases "boring".
- Delivers value more frequently.
- Get fast feedback on what users care about.

4. What is CI/CD Pipeline
- Adalah kumpulan langkah-langkah yang harus dilakukan untuk deliver version software yang lebih baru.

Biasanya, **pipeline stages** include:
- Source - Checkout code from SCM (Github, etc)
- Build - Stage di mana aplikasi dicompile
- Test - Stage di mana aplikasi di test
- Deploy - Stage di mana aplikasi di deploy

https://www.katalon.com/resources-center/blog/ci-cd-pipeline/

5. CI/CD Tools (Jenkins)
- Jenkins, CircleCI, TeamCity, Bamboo, GitLab, AzureDevOps, etc.

What is Jenkins?
- CI/CD Tools, continuous integration and build server.
- It is used to manually, periodically, or automatically build software development projecs.
- It is an open source Continous Integragion tool written in Java.
- Jenkins is used by teams of all different sizes, for projects with various languages.


Di tiket.com:
App Repo >>> Jenkins >>> Packer >>> Terraform & Ansible >>> Base Image >>> App Image 

6. Hands on Demo
https://github.com/sidiqputra/technoscape-demo/tree/main/docs/demo-day1


# Sesi 2 - 25 Juni 2021

## Jenkins Pipeline
- Harusnya kita gk boleh langsung push ke main code kyk kemarin. Harusnya ada unit test dulu, ada branching di githubnya. Kalo udah oke, baru boleh dimerge.
- Jenkins ada 2 model pipeline, **Declarative Pipeline (dengan pipeline)** dan **Scripted Pipeline (node)**

Kalo declarative, agentnya bisa beda-beda, kalo scripted agentnya harus ditentuin di awal.
Declarative ini lebih baru.


## What is unit testing
- Memastikan software bekerja dengan baik dan sesuai keinginan user.

https://github.com/sidiqputra/technoscape-demo/tree/main/docs/demo-day2













































