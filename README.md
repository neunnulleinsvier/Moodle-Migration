# Readme

## Projektübersicht

Das Ziel dieses Projekts ist es, eine bestehende Moodle-Instanz auf eine Docker-Instanz zu migrieren. Durch die Verwendung von Docker können wir die Bereitstellung, Skalierbarkeit und Portabilität der Moodle-Instanz verbessern.

## Voraussetzungen

- Installierte Docker-Engine auf dem Zielserver.
- Zugriff auf die bestehende Moodle-Instanz.
- Bereitstellung der Moodle-Datenbank, idealerweise als SQL-Dump oder Backup.
- Aktualisierte Konfigurationsdateien der Moodle-Instanz (config.php, config-dist.php usw.).
- Verständnis der grundlegenden Docker-Konzepte und -Befehle.

## Schritte zur Migration

1. **Vorbereitung:** Stellen Sie sicher, dass alle Voraussetzungen erfüllt sind und Sie über die erforderlichen Zugriffsrechte verfügen.

2. **Docker-Setup:** Installieren Sie Docker auf dem Zielserver, falls noch nicht geschehen. Stellen Sie sicher, dass Docker ordnungsgemäß ausgeführt wird und dass Sie Docker-Befehle ausführen können.

3. **Docker-Compose-Datei erstellen:** Erstellen Sie eine `docker-compose.yml`-Datei im Zielverzeichnis. In dieser Datei werden die Konfigurationen für die Docker-Container definiert. Stellen Sie sicher, dass alle erforderlichen Container und deren Abhängigkeiten, wie z.B. Datenbank-Container, richtig konfiguriert sind.

4. **Moodle-Dateien kopieren:** Kopieren Sie die Moodle-Dateien von der bestehenden Instanz in das entsprechende Verzeichnis im Docker-Container. Achten Sie darauf, dass die Verzeichnisstruktur beibehalten wird.

5. **Datenbank migrieren:** Importieren Sie die Moodle-Datenbank in den Datenbank-Container. Verwenden Sie dazu den SQL-Dump oder das Backup der bestehenden Moodle-Instanz. Aktualisieren Sie gegebenenfalls die Zugangsdaten in der Konfigurationsdatei des Moodle-Containers.

6. **Konfiguration anpassen:** Passen Sie die Konfigurationsdateien des Moodle-Containers an. Überprüfen Sie insbesondere die Datenbankverbindungseinstellungen und andere erforderliche Konfigurationsoptionen.

7. **Docker-Container erstellen und starten:** Führen Sie den Befehl `docker-compose up -d` aus, um die Docker-Container zu erstellen und zu starten. Überprüfen Sie die Protokolle, um sicherzustellen, dass alle Container erfolgreich gestartet wurden.

8. **Testen der Moodle-Instanz:** Öffnen Sie einen Webbrowser und navigieren Sie zur Adresse der Moodle-Instanz. Führen Sie verschiedene Tests durch, um sicherzustellen, dass die Migration erfolgreich war und die Moodle-Instanz ordnungsgemäß funktioniert.

9. **Dokumentation:** Aktualisieren Sie dieses Readme-Dokument mit den durchgeführten Schritten, einschließlich aller Abweichungen oder spezifischer Anpassungen, die vorgenommen wurden.

## Autoren

- Tim
- Paul
- Silas

## Lizenz

Dieses Projekt ist unter der [MIT-Lizenz](https://opensource.org/licenses/MIT) lizenziert. Weitere Informationen finden Sie in der Date
