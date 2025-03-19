I use this to load this data 
SHOW VARIABLES LIKE 'secure_file_priv';
LOAD DATA INFILE 'C:/ProgramData/MySQL/MySQL Server x.x/Uploads/PS_20174392719_1491204439457_log.csv'
INTO TABLE transactions
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
use bank

CREATE TABLE transactions ( step INT, type VARCHAR(20), amount DECIMAL(15,2), nameOrig VARCHAR(20), oldbalanceOrg DECIMAL(15,2), newbalanceOrig DECIMAL(15,2), nameDest VARCHAR(20), oldbalanceDest DECIMAL(15,2), newbalanceDest DECIMAL(15,2), isFraud TINYINT, isFlaggedFraud TINYINT );

As this is large dataset I used SQL command line interpreter to execute this queries
