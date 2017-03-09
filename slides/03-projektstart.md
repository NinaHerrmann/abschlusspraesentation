# Projektstart

## Zeitverlauf

<div>
<img alt="zeitstrahl" align="middle" src="images/zeitstrahl.png">
</div>

---

## Vorgehensweise

* Zunächst die Überlegung mit Open Cloud Mesh zu arbeiten
	* Serverunabhängige sync & share Architektur zwischen clouds
		* Zu unausgereift und zu viele Bugs übrig, um für dieses Projektseminar relevant zu sein
* Abwägung der passwortlosen Authentifizierungsmöglichkeiten
	* JSON Web Tokens, Macaroons, SSO, <font color=red>OAuth2</font>
		* OAuth2 kombiniert passwortlose Authentifizierung für den Client und
		steuert diese zusammen mit der Autorisierung über einen Access Token.
		* Umfang und Dauer der Autorisierung kann eingeschränkt werden
		* Entzug der Autorisierung pro Client steuerbar
* Evaluation der vorhandenen moodle Plugins
	* Dropbox
		* nutzt OAuth2 als API Absicherung
		* ownCloud unterstützt OAuth jedoch noch nicht
		* andere API als ownCloud -> nützlicher Ansatz, aber keine Kompatibilität
	* WebDAV
		* moodle als WebDAV Client für Datenübermittlung
		* ownCloud verfügt über WebDAV Integration, dessen Funktionalitäten erweitert werden können
		* kein OAuth

---

# Allgemeiner OAuth 2.0 Protokollablauf

<div align="center">
	<img alt="OAuth Allgemein" src="images/oauth-allgemein.svg" width=85%>
</div>

---

## moodle Plugin Architektur

<div class="todo">Todo: Bild der Pluginarchitektur einfuegen</div>
