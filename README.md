# Network-Infrastructure

Virtualized Network Infrastructure with Kubernetes & LDAP

📌 Overview

This project simulates a small enterprise IT infrastructure using VMware Workstation with multiple VMs.
It integrates core services (DNS, Mail, NFS, Automation) with centralized authentication (LDAP) and a Kubernetes cluster for scalable web applications.
The goal is to combine traditional Unix/Linux system administration with modern DevOps orchestration practices.

🗂️ Architecture

	OpenBSD (192.168.88.1): DNS + LDAP (central identity provider).

	FreeBSD (192.168.88.2): Mail Server (LDAP authentication).

	Rocky Linux (192.168.88.3): NFS Server (LDAP authentication).

	Ubuntu (192.168.88.4): Kubernetes Master (control plane, LDAP authentication).
	
	Runs control plane components (kube-apiserver, etcd, controller-manager, scheduler).

	Manages worker nodes hosting web applications.

	Solaris (192.168.88.5): Automation and centralized login management with Ansible.

Each VM includes a failsafe local account in case LDAP is unavailable.

📊 Diagram

<img width="602" height="449" alt="image" src="https://github.com/user-attachments/assets/f7bfadfa-ac3d-4eb3-8abf-0e27b27d7a31" />



⚙️ Features

	Centralized authentication via LDAP.
	
	DNS management with OpenBSD.
	
	Distributed services: Mail, NFS, Automation.
	
	Kubernetes cluster for containerized web servers (scalable + fault-tolerant).
	
	Hybrid approach: traditional servers + cloud-native orchestration.



🔮 Future Improvements

	Add monitoring with Prometheus + Grafana.
	
	Integrate CI/CD with GitLab or GitHub Actions.
	
	Deploy real-world applications (e.g., WordPress, Flask/Django apps) on the Kubernetes cluster.

👨‍💻 Author

Carlos D. Martinez
Computer Science, SDSU
Interested in DevOps, Cloud, and Infrastructure Engineering.
