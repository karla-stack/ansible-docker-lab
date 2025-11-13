# Práctica Ansible - Automatización Servidor Web

Este proyecto automatiza la instalación y configuración de servidores web **nginx** usando **Ansible** y **Docker**.

## 🎯 Objetivo
Aprender a usar Ansible para automatizar la configuración de múltiples servidores de forma simultánea.

## 🛠️ Tecnologías
- Docker & Docker Compose
- Ansible
- Nginx
- Ubuntu 24.04

## 📁 Estructura del proyecto
```
ansible-docker-lab/
├── Dockerfile              # Imagen base de Ubuntu con SSH
├── docker-compose.yml      # Configuración de los contenedores
├── inventory.ini           # Inventario de servidores para Ansible
├── playbook.yml            # Playbook que instala y configura nginx
├── ansible.cfg             # Configuración de Ansible
└── site/
    └── index.html          # Página web personalizada
```

## 🚀 Instrucciones de uso

### 1. Levantar los contenedores
```bash
docker compose up --build -d
```

### 2. Ejecutar Ansible (desde node1)
```bash
docker exec -it node1 bash
apt update && apt install -y ansible sshpass
```

### 3. Crear archivos de configuración dentro del contenedor
```bash
# Ver instrucciones completas en el repositorio
```

### 4. Ejecutar el playbook
```bash
ansible-playbook -i /home/ansible/inventory.ini /home/ansible/playbook.yml
```

### 5. Verificar en el navegador
- http://localhost:8081
- http://localhost:8082

## ✅ Resultado
Los dos servidores mostrarán la página: **"Hola desde Ansible!"**

## 👤 Autor
Karla Stack - Práctica de Ansible con Docker
