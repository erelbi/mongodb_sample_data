# MongoDB Training Data


> sample_airbnb
> sample_analytics
> sample_geospatial
> sample_mflix
> sample_restaurants
> sample_training
> sample_weatherdata

## Clone
```sh
git clone https://github.com/erelbi/mongodb_sample_data.git
```
### output
```output
Cloning into 'mongodb_sample_data'...
remote: Enumerating objects: 57, done.
remote: Counting objects: 100% (57/57), done.
remote: Compressing objects: 100% (46/46), done.
remote: Total 57 (delta 3), reused 57 (delta 3), pack-reused 0
Receiving objects: 100% (57/57), 76.74 MiB | 1.81 MiB/s, done.
Resolving deltas: 100% (3/3), done.
Updating files: 100% (41/41), done.
```
## Restore
```sh
cd mongodb_sample_data/
mongorestore --db sample_airbnb sample_airbnb/sample_airbnb/ &&
mongorestore --db sample_analytics sample_analytics/sample_analytics/ &&
mongorestore --db sample_geospatial sample_geospatial/sample_geospatial/ &&
mongorestore --db sample_mflix sample_mflix/sample_mflix/ &&
mongorestore --db sample_restaurants sample_restaurants/sample_restaurants/ &&
mongorestore --db sample_training sample_training/sample_training/ &&
mongorestore --db sample_weatherdata sample_weatherdata/sample_weatherdata/ &&
```
```
> show dbs
admin               0.000GB
config              0.000GB
local               0.000GB
sample_airbnb       0.051GB
sample_analytics    0.009GB
sample_geospatial   0.001GB
sample_mflix        0.040GB
sample_restaurants  0.006GB
sample_training     0.039GB
sample_weatherdata  0.002GB
```
```json
[root@fedora mongodb_sample_data]# mongo --quiet --eval  "printjson(db.adminCommand('listDatabases'))"
{
	"databases" : [
		{
			"name" : "admin",
			"sizeOnDisk" : 40960,
			"empty" : false
		},
		{
			"name" : "config",
			"sizeOnDisk" : 110592,
			"empty" : false
		},
		{
			"name" : "local",
			"sizeOnDisk" : 40960,
			"empty" : false
		},
		{
			"name" : "sample_airbnb",
			"sizeOnDisk" : 55029760,
			"empty" : false
		},
		{
			"name" : "sample_analytics",
			"sizeOnDisk" : 9904128,
			"empty" : false
		},
		{
			"name" : "sample_geospatial",
			"sizeOnDisk" : 983040,
			"empty" : false
		},
		{
			"name" : "sample_mflix",
			"sizeOnDisk" : 43069440,
			"empty" : false
		},
		{
			"name" : "sample_restaurants",
			"sizeOnDisk" : 6230016,
			"empty" : false
		},
		{
			"name" : "sample_training",
			"sizeOnDisk" : 42274816,
			"empty" : false
		},
		{
			"name" : "sample_weatherdata",
			"sizeOnDisk" : 2490368,
			"empty" : false
		}
	],
	"totalSize" : 160174080,
	"ok" : 1
}
```




