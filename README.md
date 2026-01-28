# test-eplc

Berikut merupakan tahapan cara penggunaan API yang sudah di-develop

## Clone
``git clone {url_project_git}``

## Composer Install
lakukan composer install untuk meng-install semua dependency yang dibtuhkan :
`composer install`

## Migrate
lakukan migrate database, sebelum itu, pastikan database sudah terbuat, saya menggunakan MySQL sebagai RDBMS dengan nama database `db_eplc` lalu : 
`php artisan migrate`

## Running
php artisan serve

## API
gunakan command ``php artisan route:list`` untuk mengetahui route apa saja yang sudah dibuat beserta Method nya

### Register 
untuk mendapatkan akun, lakukan terlebih dahulu registrasi, berikut curl dan contoh body :
`postman request POST 'http://localhost:8000/api/register' \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --header 'Cookie: XSRF-TOKEN=eyJpdiI6IndXTlBrZlIzblpiWWZ6Y1Z5NzVxTHc9PSIsInZhbHVlIjoidGVjTVdPei81VmtaRkxqRXJVYUtRN0M3RzhKRWwwV2hCZnFkekVhY1oxV2tsYzVPTitKa0VDbTduMWlGMkJyQ0hYNDJ6aG5xV3c2UWJjeW9UNU1JNDlvTEpsUVNUV3RlUmNmSEkvZmttbmxJZTRRK0R6RGhvd2h3RldDQWZQUlAiLCJtYWMiOiI4NDJiNDY5NjA2M2I2NDAyZjA5Y2Q3YmEwMGQ3ZWVkMTg1ZmNmMjJlYTk0ZjA2ZDc2MjIzZmY4OGQyM2ExZmFmIiwidGFnIjoiIn0%3D; laravel_session=eyJpdiI6InJTWVV0OWJUNjdkUWdFR1hKWEJ1cFE9PSIsInZhbHVlIjoiakdPTWhyM2NpOVRBbFBGNzlOQWNpUUFYRzNKMkVqQjJRVjdEUk9pUkRxZzg4b1pPV2xCNlJITHp1Q2o3YmxMenh3SnpPVTVBNWJFaGhIeWdRSm1sN3FieUdyOUIxKzJXSTk1S3l2K0xLcXJwRXF3ZlBLZXZEVFh1OVZ3dm4zb1ciLCJtYWMiOiI3NmI4Y2FiMWFlYjljNmFlZjgyN2QwZjA4NzViOTY2NThjZTMzN2E5NmFmMjdiMTgxMjBmYmEzY2ZhZWMyYjI2IiwidGFnIjoiIn0%3D' \
  --body '{
    "name": "Dea Agnia",
    "email": "deaagnia@gmail.com",
    "password": "pass123",
    "password_confirmation": "pass123"
}'`

### Login
berikut contoh curl, beserta body nya :

`postman request POST 'http://localhost:8000/api/login' \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --header 'Cookie: XSRF-TOKEN=eyJpdiI6IndXTlBrZlIzblpiWWZ6Y1Z5NzVxTHc9PSIsInZhbHVlIjoidGVjTVdPei81VmtaRkxqRXJVYUtRN0M3RzhKRWwwV2hCZnFkekVhY1oxV2tsYzVPTitKa0VDbTduMWlGMkJyQ0hYNDJ6aG5xV3c2UWJjeW9UNU1JNDlvTEpsUVNUV3RlUmNmSEkvZmttbmxJZTRRK0R6RGhvd2h3RldDQWZQUlAiLCJtYWMiOiI4NDJiNDY5NjA2M2I2NDAyZjA5Y2Q3YmEwMGQ3ZWVkMTg1ZmNmMjJlYTk0ZjA2ZDc2MjIzZmY4OGQyM2ExZmFmIiwidGFnIjoiIn0%3D; laravel_session=eyJpdiI6InJTWVV0OWJUNjdkUWdFR1hKWEJ1cFE9PSIsInZhbHVlIjoiakdPTWhyM2NpOVRBbFBGNzlOQWNpUUFYRzNKMkVqQjJRVjdEUk9pUkRxZzg4b1pPV2xCNlJITHp1Q2o3YmxMenh3SnpPVTVBNWJFaGhIeWdRSm1sN3FieUdyOUIxKzJXSTk1S3l2K0xLcXJwRXF3ZlBLZXZEVFh1OVZ3dm4zb1ciLCJtYWMiOiI3NmI4Y2FiMWFlYjljNmFlZjgyN2QwZjA4NzViOTY2NThjZTMzN2E5NmFmMjdiMTgxMjBmYmEzY2ZhZWMyYjI2IiwidGFnIjoiIn0%3D' \
  --body '{
    "email": "deaagnia@gmail.com",
    "password": "pass123"
}'`
