# Stage ingénieur automaticien — Sounduct (Strasbourg)

> Stage orienté automatisation / digitalisation atelier : IHM Python connectées ERP, traçabilité QR, vision embarquée (Raspberry Pi) et automatisation via robot collaboratif.

---

## Aperçu
- Développé des IHM en Python connectées à l’ERP pour digitaliser et fiabiliser les opérations de l’atelier.
- Mise en place un système de traçabilité par codes QR (génération/lecture, suivi des flux, remontée d’informations).
- Conçu une application de vision embarquée sur Raspberry Pi pour détecter automatiquement les bacs vides.
- Implémenté et entraîné des modèles de détection/vision avec OpenCV et TensorFlow / PyTorch.
- Automatisé l’action correctrice en envoyant des ordres au robot collaboratif MyCobot pour le remplacement des bacs via le pipeline Python.

---

## Démo & livrables
- Vidéos (Drive) : LIEN_DRIVE_VIDEOS
- PDF / rapport (Drive) : LIEN_DRIVE_PDF
- Images (Drive) : LIEN_DRIVE_IMAGES


---

## Stack
- Logiciel : Python, Tkinter, OpenCV
- IA / Vision : TensorFlow, PyTorch
- Embarqué : Raspberry Pi, Linux
- Traçabilité : QR codes (génération/lecture)
- Robotique : MyCobot (envoi d’ordres / automatisation)
- ERP (connexion et échanges)

---

## Architecture (vue simple) 
```mermaid
flowchart LR
  A[Opérateur / Atelier] --> B[IHM Python (Tkinter)]
  B <--> C[ERP]
  A --> D[QR Code Scan/Gen]
  D --> B

  E[Caméra] --> F[Raspberry Pi]
  F --> G[Pipeline Vision (OpenCV + modèle IA)]
  G --> H{Bac vide ?}
  H -- Oui --> I[Ordre robot MyCobot]
  H -- Non --> J[Monitoring / Logs]
