# TP Data Mining L2 – Collecte et Fusion Multi-Sources

## Objectif du projet
Ce projet a pour objectif de **collecter et fusionner des données provenant de plusieurs sources** afin de préparer un pipeline KDD (Knowledge Discovery in Databases).  
Les données proviennent de fichiers locaux, d'une base de données MySQL, d'une API publique et d'un site web via Web Scraping.

---

## Sources de données utilisées

1. **Fichiers locaux**  
   - CSV : `student_performance.csv` contenant les informations des étudiants (id, notes, participation, etc.)  
   - JSON : `movies.json` contenant des informations sur des films  
   - Excel : `DataProjet.xlsx` avec certaines colonnes sélectionnées

2. **Base de données MySQL**  
   - Connexion à la base `school_db` pour récupérer les étudiants ayant une colonne spécifique (`COL 5`) supérieure à 50.

3. **Web Scraping**  
   - Site : [Books to Scrape](https://books.toscrape.com/)  
   - Extraction des **titres de livres** présents sur la page principale  
   - Lecture préalable du fichier `robots.txt` pour vérifier l’autorisation de scraping

4. **API publique**  
   - API : [JSONPlaceholder Users](https://jsonplaceholder.typicode.com/users)  
   - Récupération des informations sur les utilisateurs (`id`, `name`, `username`, `email`, `phone`) et conversion en **DataFrame**

---

## Bibliothèques nécessaires
Pour exécuter le script et le Notebook, installez les librairies suivantes :

```bash
pip install pandas requests beautifulsoup4 sqlalchemy pymysql openpyxl