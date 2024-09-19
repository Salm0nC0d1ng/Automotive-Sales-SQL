DROP TABLE IF EXISTS customers;
DROP TABLE IF EXISTS vehicles;
DROP TABLE IF EXISTS salespersons;
DROP TABLE IF EXISTS sales;
DROP TABLE IF EXISTS dealerships;

CREATE TABLE customers (
    customerID INT PRIMARY KEY,
    firstName VARCHAR(255),
    lastName VARCHAR(255),
    email VARCHAR(255),
    phoneNumber VARCHAR(255),
    address VARCHAR(255),
    city VARCHAR(255)
);

CREATE TABLE vehicles (
  vehicleID INT PRIMARY KEY,
  manufacturer VARCHAR(255),
  model VARCHAR(255),
  year VARCHAR(255),
  licensePlate VARCHAR(255),
  color VARCHAR(255),
  price FLOAT,
  stock INT
);

CREATE TABLE salespersons (
  salespersonsID INT PRIMARY KEY,
  firstName VARCHAR(255),
  lastName VARCHAR(255),
  email VARCHAR(255),
  phoneNumber VARCHAR(255),
  hireDate DATE
);

CREATE TABLE sales (
  salesID INT PRIMARY KEY,
  salesDate DATE,
  salesPrice FLOAT,
  paymentMethod varchar,
  customerID int,
  vehicleID int,
  salespersonsID int
);

CREATE TABLE dealerships (
  dealershipID INT PRIMARY KEY,
  dealershipName VARCHAR(255),
  location VARCHAR(255),
  phoneNumber VARCHAR(255),
  managerID INT
);

INSERT INTO customers (customerID, firstName, lastName, email, phoneNumber, address, city) VALUES
(1, 'Bartholomeo', 'Longworthy', 'blongworthy0@merriam-webster.com', '204-703-7117', 'Room 456', 'Rosebank'),
(2, 'Zorine', 'Child', 'zchild1@digg.com', '431-898-1810', '9th Floor', 'New Sibonga'),
(3, 'Bren', 'Adamski', 'badamski2@alibaba.com', '281-703-5430', '10th Floor', 'Laboulaye'),
(4, 'Ricardo', 'Prattin', 'rprattin3@amazon.com', '112-256-3826', '15th Floor', 'Hennenman'),
(5, 'Emilio', 'Claw', 'eclaw4@tripadvisor.com', '770-843-1615', '3rd Floor', 'Siemianowice Śląskie'),
(6, 'Willabella', 'Tonner', 'wtonner5@chronoengine.com', '392-349-0197', 'Room 854', 'Maguyam'),
(7, 'Chico', 'Hindmore', 'chindmore6@multiply.com', '796-619-6668', 'Suite 73', 'Bāniyās'),
(8, 'Consuelo', 'Willoughby', 'cwilloughby7@tumblr.com', '979-195-6006', 'PO Box 64685', 'Uvarovo'),
(9, 'Mirella', 'Ondrus', 'mondrus8@friendfeed.com', '768-675-4110', 'Room 1945', 'Vsevolozhsk'),
(10, 'Gillie', 'Fellenor', 'gfellenor9@bandcamp.com', '742-935-0000', 'Suite 47', 'Tumpang');
INSERT INTO vehicles (vehicleID, manufacturer, model, year, licensePlate, color, price, stock) VALUES
(1, 'Honda', 'Ridgeline', 2010, '3G5DB03E72S308630', 'Green', 62867.43, 5),
(2, 'Toyota', 'Previa', 1991, 'WAUMFAFL0DN720167', 'Violet', 91247.18, 1),
(3, 'Toyota', 'Sequoia', 2001, '1G6DV5EP6B0339499', 'Orange', 69855.58, 9),
(4, 'Pontiac', 'Bonneville', 2000, 'JN1CV6EK9FM588108', 'Violet', 93243.42, 9),
(5, 'Ford', 'F-Series', 1986, '5LMJJ2JT1FE931844', 'Turquoise', 78707.20, 4),
(6, 'Mazda', '626', 1995, 'JTHBK1GG5F2376023', 'Goldenrod', 51221.78, 1),
(7, 'Saturn', 'L-Series', 2005, 'WAUBFAFL7AN927870', 'Red', 88418.94, 2),
(8, 'Lexus', 'GS', 2013, '2HNYD18766H502671', 'Turquoise', 72404.51, 7),
(9, 'Dodge', 'Ram 1500', 1999, 'WDDJK7DA1FF532041', 'Indigo', 49691.29, 10),
(10, 'Dodge', 'Ram 1500', 1998, 'YV4940BL7D1664912', 'Fuscia', 20582.85, 10);
INSERT INTO sales (salesID, salesDate, salesPrice, paymentMethod, salespersonsID, customerID, vehicleID) VALUES
(1, '2024-03-29', 66983.31, 'diners-club-enroute', 2, 3, 9),
(2, '2024-09-14', 41646.17, 'diners-club-carte-blanche', 10, 5, 1),
(3, '2023-10-03', 88006.06, 'jcb', 7, 6, 4),
(4, '2024-06-05', 65459.68, 'mastercard', 10, 10, 3),
(5, '2024-06-01', 23352.40, 'jcb', 5, 9, 10),
(6, '2024-06-26', 32621.59, 'jcb', 6, 8, 9),
(7, '2024-03-30', 76777.54, 'visa-electron', 3, 5, 8),
(8, '2023-11-24', 92587.74, 'mastercard', 10, 5, 5),
(9, '2024-02-18', 23021.49, 'jcb', 2, 7, 5),
(10, '2023-10-29', 88342.52, 'diners-club-enroute', 2, 4, 6);
INSERT INTO salespersons (salespersonsID, firstName, lastName, email, phoneNumber, hireDate) VALUES
(1, 'Kristy', 'Blunsum', 'kblunsum0@newyorker.com', '279-269-1256', '2022-04-26'),
(2, 'Pascal', 'Grason', 'pgrason1@vkontakte.ru', '518-754-1613', '2021-11-21'),
(3, 'Edwin', 'Di Antonio', 'ediantonio2@163.com', '661-833-6520', '2021-07-30'),
(4, 'Tanitansy', 'Roseborough', 'troseborough3@skype.com', '843-102-1042', '2020-12-29'),
(5, 'Tammara', 'Beagan', 'tbeagan4@utexas.edu', '261-276-3137', '2019-04-04'),
(6, 'Carlynn', 'Feak', 'cfeak5@yahoo.com', '426-533-7844', '2023-12-04'),
(7, 'Ailis', 'Kays', 'akays6@opensource.org', '411-451-0044', '2018-01-18'),
(8, 'Jedediah', 'Rossin', 'jrossin7@moonfruit.com', '483-275-7695', '2019-02-16'),
(9, 'Malena', 'Barends', 'mbarends8@fema.gov', '465-583-5958', '2023-01-21'),
(10, 'Claudine', 'Guilaem', 'cguilaem9@technorati.com', '430-189-2928', '2023-01-07');
INSERT INTO dealerships (dealershipID, dealershipName, location, phoneNumber, managerID) VALUES
(1, 'Gavra', 'Shadrach', '527-275-0284', 5),
(2, 'Twyla', 'Simenet', '183-925-4645', 8),
(3, 'Caz', 'Swatman', '248-481-6090', 5),
(4, 'Goldina', 'Wharmby', '193-896-7558', 7),
(5, 'Othello', 'Bugs', '155-919-7059', 5),
(6, 'Flossi', 'Leggat', '808-724-3362', 1),
(7, 'Pamella', 'Dockrey', '619-508-1956', 6),
(8, 'Spenser', 'Thornley', '335-944-9122', 4),
(9, 'Elvin', 'Mengo', '981-741-7723', 7),
(10, 'Gayla', 'Valerius', '658-259-2704', 5);
