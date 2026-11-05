# Sicherheitsmeldungen

Bitte keine API-Tokens, Schülerdaten, Konfigurationsdateien oder Anmeldelinks in öffentlichen Issues, Screenshots oder Logs veröffentlichen.

Für vertrauliche Meldungen ist die GitHub-Funktion **Security → Advisories → Report a vulnerability** vorgesehen. Vor Veröffentlichung muss der Repository-Eigentümer diese Funktion aktivieren und ihre Erreichbarkeit prüfen. Solange der Meldeknopf fehlt, ist dieser private Meldeweg noch nicht eingerichtet; bitte keine Sicherheitsdetails öffentlich einstellen.

Eine Meldung sollte die App-Version, Windows-Version, eine Beschreibung der Auswirkungen und Reproduktionsschritte mit synthetischen Daten enthalten. Keine echten Zugangsdaten mitsenden.

Sicherheitskorrekturen werden für die jeweils aktuelle veröffentlichte Version vorgesehen; für ältere Versionen gibt es keine zugesagte Pflegefrist oder Reaktionszeit.

Die Windows-Ausgabe bindet an Loopback, prüft Host und Herkunft von Schreibzugriffen und verlangt eine lokale Sitzung. DPAPI schützt gespeicherte Tokens im Windows-Benutzerkontext. Das Windows-Paket enthält keine eigene EXE, sondern die unveränderte, von der OpenJS Foundation signierte `node.exe` und die App als `app.js`. Smart App Control prüft diese Skriptdatei nicht. Eine manipulierte Kopie fällt deshalb nicht durch eine ungültige Signatur auf: Pakete nur von der offiziellen Release-Seite laden, Prüfsummen vergleichen und den Link statt der Datei weitergeben.

Administratoren, Schadsoftware im Benutzerkonto und nicht vertrauenswürdige lokale Webdienste liegen außerhalb der zugesicherten Schutzgrenze. Weitere Betriebsgrenzen stehen in `ENTWICKLUNG.md` im Quellcode-ZIP unter „Sicherheit & Robustheit“.

Einrichtung des Meldewegs: [GitHub-Dokumentation zum privaten Melden von Schwachstellen](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/configure-vulnerability-reporting/configure-for-a-repository).
