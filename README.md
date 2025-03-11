# Wichtige Befehle für Serververwaltung

## Certbot (Let's Encrypt)
### Installation
```bash
sudo apt update
sudo apt install certbot python3-certbot-nginx
```

### SSL-Zertifikat erstellen
```bash
sudo certbot --nginx -d example.com -d www.example.com
```

### Zertifikat erneuern
```bash
sudo certbot renew --dry-run
```

### Zertifikate anzeigen
```bash
sudo certbot certificates
```

### Zertifikat manuell erneuern
```bash
sudo certbot renew
```

## NGINX
### Installation
```bash
sudo apt update
sudo apt install nginx
```

### NGINX starten/stoppen/neustarten
```bash
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
```

### Konfiguration testen
```bash
sudo nginx -t
```

### Logs anzeigen
```bash
sudo tail -f /var/log/nginx/access.log
sudo tail -f /var/log/nginx/error.log
```

## PM2 (Process Manager für Node.js)
### Installation
```bash
npm install -g pm2
```

### Anwendung starten
```bash
pm2 start app.js --name myApp
```

### Anwendung stoppen
```bash
pm2 stop myApp
```

### Anwendung neu starten
```bash
pm2 restart myApp
```

### Alle laufenden Prozesse anzeigen
```bash
pm2 list
```

### PM2-Prozesse beim Systemstart starten lassen
```bash
pm2 startup
```

### Logs anzeigen
```bash
pm2 logs
```

## MySQL
### MySQL-Server starten/stoppen
```bash
sudo systemctl start mysql
sudo systemctl stop mysql
sudo systemctl restart mysql
```

### MySQL-Konsole aufrufen
```bash
mysql -u root -p
```

### Datenbanken anzeigen
```sql
SHOW DATABASES;
```

### Benutzer erstellen
```sql
CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
```

### Rechte vergeben
```sql
GRANT ALL PRIVILEGES ON database_name.* TO 'username'@'localhost';
FLUSH PRIVILEGES;
```

### MySQL-Dienststatus prüfen
```bash
sudo systemctl status mysql
```

---
Falls weitere Befehle oder Technologien hinzugefügt werden sollen, einfach ergänzen!

