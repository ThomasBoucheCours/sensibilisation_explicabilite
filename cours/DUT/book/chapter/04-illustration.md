# Exemple pour illustrer le cours
Pour illustrer les méthodes, utilisation du jeu de données [ERA5-Land hourly data from 1950 to present](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land?tab=download)

Ce Dataset ERA5 fournit des données météo horaires depuis 1950, partout dans le monde, en combinant des mesures réelles (stations météo, satellites, etc.) et un modèle informatique pour recréer les conditions climatiques.

Les variables extraites :
- `d2m` : Température du point de rosée à 2 mètres au-dessus du sol, en degrés Celsius (°C).
- `t2m` : Température de l'air à 2 mètres au-dessus du sol, en degrés Celsius (°C).
- `ssrd` : Rayonnement solaire direct qui atteint la surface de la Terre, en watts par mètre carré (W/m²).
- `sp` : Pression atmosphérique au niveau de la mer, en hectopascals (hPa).
- `tp` : Précipitations totales, en millimètres (mm).
- `latitude` : latitude
- `longitude` : longitude
- `hour` : heure de l'observation

- `wind_speed` : La vitesse de vent (km/h) --> cette variable a été reconstruite à partir de `u10` la composante horizontale (ouest-est) de la vitesse du vent. Et de `v10`, la composante verticale (sud-nord) de la vitesse du vent.