# Carnet de Données - Projet Field Scan

## Sentinel-2 L2A (Copernicus), côte de l'Équateur
- Accès : copie publique Copernicus sur Microsoft Planetary Computer (STAC)
- Licence : libre accès Copernicus. Mention : « Contains modified Copernicus Sentinel data 2026 »
- Zone : carré d'environ 9 km de côté près d'El Guabo (El Oro), bbox [-79.86, -3.32, -79.78, -3.24]
  (région bananière supposée, à confirmer sur une image de fond)
- Tuile : T17MPS, système de coordonnées EPSG:32717
- Saison sèche : S2C_MSIL2A_20260808T153631_R068_T17MPS_20260808T212312 (8 août 2026)
  pixels valides après masque : 97 %
- Saison des pluies : image du 10 avril 2026, T17MPS_20260410T204104 (identifiant complet : voir le notebook)
  pixels valides après masque : 94 %. Pixels communs aux deux dates : 91 %
- Bandes : B04 (rouge) et B08 (infrarouge proche) à 10 m ; B8A et B11 (infrarouge à ondes courtes) à 20 m ;
  SCL (classification de la scène) à 20 m, ramenée à 10 m pour le NDVI
- Masque : seuls les pixels « végétation » et « sol nu » (classes SCL 4 et 5) sont gardés
- Réflectance : (valeur - 1000) / 10000 (décalage à confirmer pour ces produits)
- Résultats : NDVI moyen 0,785 (sèche) et 0,758 (pluies) sur les pixels communs
- Limites :
  - une seule date par saison, et aucune vérité terrain : validation par cohérence physique uniquement
  - résolution de 10 m, insuffisante pour compter des pieds
  - le NDVI sature sur une végétation dense, d'où le NDMI
  - un premier choix d'image avait 33 % de pixels « sans donnée » (bord de la bande) : écarté
- Sorties : ndvi_seche_2026-08-08.tif, ndvi_pluies_2026-04-10.tif et leur différence (GeoTIFF, Drive)
