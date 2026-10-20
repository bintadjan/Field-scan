import os

# 1. Créer le dossier src/ s'il n'existe pas
os.makedirs("src", exist_ok=True)
print("Dossier 'src/' créé avec succès !")

# 3. Créer le fichier data_card.md
datacard_content = """# Carnet de Données - Projet Field Scan

## 1. Imagerie Satellitaire (Sentinel-2)
* **Source :** Copernicus Browser / ESA
* **Licence :** Open Data Copernicus (CC BY 4.0)
* **Résolution :** 10 mètres par pixel (bandes RVB et NIR)
* **Date d'acquisition :** Mars 2026 (Saison des pluies) & Juin-Août 2026 (Saison sèche)
* **Projection / CRS :** EPSG:32717
* **Biais et limites :** Présence de nuages sur certaines tuiles (filtrage nécessaire) ; résolution de 10m insuffisante pour compter les pieds individuels (réservée à l'analyse de vigueur/stress global).

## 2. Dataset Maladies Foliaires (Tanzanie & BananaLSD)
* **Source :** Harvard Dataverse (Banana Leaves Imagery Dataset) & BananaLSD
* **Licence :** Creative Commons (CC BY)
* **Composition :** ~5 600 images saines et ~5 700 images de Black Sigatoka (Tanzanie) + dataset BananaLSD (cordana, pestalotiopsis, etc.).
* **Résolution / Type :** Photos de terrain prises de près (smartphone/appareil photo au sol).
* **Biais et limites (Domain Gap) :** Écart important entre ces images prises au sol et de près, et les vues aériennes de drone ou satellite. Le modèle devra être utilisé comme un outil d'aide au diagnostic local.
"""

with open("data_card.md", "w", encoding="utf-8") as f:
    f.write(datacard_content)
print("Fichier 'data_card.md' créé avec succès !")
