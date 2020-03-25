
##Script's
firebase-import --database_url https://mahotacrm.firebaseio.com --path /funcionarios --json data.json --merge --service_account serviceAccountKey.json

firebase-import --database_url https://mahotacrm.firebaseio.com --path /localizacoes --json localizacoes.json  --service_account serviceAccountKey.json

firebase-import --database_url https://mahotacrm.firebaseio.com --path /localizacoes --json localizacoes.json  --service_account serviceAccountKey.json

--database_url https://mahotacrm.firebaseio.com --path / --json d.json --merge --service_account serviceAccountKey.json --force

https://medium.com/@impaachu/how-to-upload-data-to-firebase-firestore-cloud-database-63543d7b34c5

Edit
data.json -> export excel to Json https://www.convertcsv.com/csv-to-json.htm

ServiceAccount -> form firebase

#Code Explanation#

Line 1: Importing firebase-admin library

Line 2: Importing service account key information

Line 4: Importing JSON data file

Line 5: Setting up collection name. please modify this line and setup your own collection name

Line 7–10: Initialising admin sdk

Line 12–14: Setting up Firestore property

Line 16: Checking if any data exists in data file and if it is object type

Line 17: Loop on data object

Line 18: Calling Firestore API to store each document

Line 19: Setting collection name

Line 20: Setting document name/key. Please do not provide document key if you want auto generated document key.


