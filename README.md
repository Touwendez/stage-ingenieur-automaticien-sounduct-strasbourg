# Stage ingénieur automaticien — Sounduct (Strasbourg)

Stage orienté automatisation / digitalisation atelier : IHM Python connectées à un ERP, traçabilité QR, vision embarquée (Raspberry Pi) et automatisation via robot collaboratif.

---

## Sommaire
- [Aperçu](#aperçu)
- [Ressources](#ressources)
- [Stack](#stack)
- [Architecture](#architecture)
- [Contributions](#contributions)
- [Compétences développées](#compétences-développées)
- [Résultats](#résultats)
- [Confidentialité](#confidentialité)
- [Aperçu visuel](#aperçu-visuel)
- [Contact](#contact)

---

## Aperçu
- Développé des IHM en Python connectées à l’ERP pour digitaliser et fiabiliser les opérations de l’atelier.
- Mis en place un système de traçabilité par codes QR (génération/lecture, suivi des flux, remontée d’informations).
- Conçu une application de vision embarquée sur Raspberry Pi pour détecter automatiquement les bacs vides.
- Implémenté et entraîné des modèles de détection/vision avec OpenCV et TensorFlow / PyTorch.
- Automatisé l’action correctrice en envoyant des ordres au robot collaboratif MyCobot pour le remplacement des bacs via un pipeline Python.

---

## Ressources
- Dossier Drive (vidéos, PDF, images) :
  - https://drive.google.com/drive/folders/1ak32aWUnkS-qCLmmsp6HQZzghjTfE-tz?usp=sharing

Recommandé : organise le Drive en sous-dossiers `videos/`, `pdf/`, `images/` (et éventuellement `captures/`).
Si tu ajoutes des images “vitrine”, mets-les dans `images/` (ou `captures/`) et utilise la section [Aperçu visuel](#aperçu-visuel).

---

## Stack
- Python (IHM, automatisation, traitement données)
- Tkinter / Qt Designer (création d’IHM)
- OpenCV
- TensorFlow, PyTorch
- Raspberry Pi, Linux
- Codes QR (génération / lecture)
- ERP (connexion & échanges)
- Robot collaboratif MyCobot (envoi d’ordres)
- CAO : SolidWorks
- Données : CSV / Excel (exploitation et consolidation sous Python)

---

## Architecture

```mermaid
flowchart LR
  A[Operateur Atelier] --> B[IHM Python]
  B <--> C[ERP]
  A --> D[QR Code Scan Generation]
  D --> B
  E[Camera] --> F[Raspberry Pi Linux]
  F --> G[Vision OpenCV Modele IA]
  G --> H{Bac vide}
  H -- Oui --> I[Commande MyCobot]
  H -- Non --> J[Logs Monitoring]



## Aperçu visuel

### IHM (Python)
![IHM - écran principal](assets/ihm_1.png)

### Vision embarquée (Raspberry Pi)
![Pipeline vision](assets/vision_pipeline.png)

### Setup
![Setup Raspberry Pi](assets/setup_rpi.jpg)
