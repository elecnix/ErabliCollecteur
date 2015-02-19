# ErabliPi

Application Node.js affichant le niveau de réservoirs d'une érablière.

## 1. Install node modules

Assuming NPM is already installed:

    npm install

## 2. Create SQLite Database

    sqlite3 erablipi.sqlite3 < schema.sql
    sqlite3 erablipi.sqlite3 -header -separator $'\t' 'select reading_date, device_name, raw_reading, gallons from tank_reading' > public/tank-levels.csv

## 3. Configure

    cp run.sh.sample run.sh

Fill run.sh with your device IDs.

Get your access token and device IDs from the spark IDE.

## 3. Run!

    ./run.sh

