create database osm

**https://imposm.org/docs/imposm/latest/tutorial.html#create-database**


create cache for lizmap:

```
docker exec -it pirate_lizmap_1 bash
cd /var/www/websig/
php lizmap/scripts/script.php lizmap~wmts:capabilities  geopoppy osm1
php lizmap/scripts/script.php lizmap~wmts:seeding -v -f  geopoppy osm1 osm EPSG:3857 0 17
lizmap/install/set_rights.sh www-data www-data

```
