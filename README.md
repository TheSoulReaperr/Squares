# Colored Squares
A simple multi-page website simulating an online market-place where multiple users can buy
“colored squares” from a single seller. The admin can add new colors while other users can buy the
colors listed by the admin. The admin will already be registered. In the home page clicking on the
username will direct to the profile page.
username: admin
password: admin
Technologies Used:
Front-End: HTML, CSS
Back-End: MariaDB (WAMP)
Client-Server Communication: Node js
Main Page : localhost:3000
Node Packages Used:
Express
Cookie-parser
MySQL
npm install express
npm install mysql
npm install cookie-parser
Back-End Details: WAMP
Username: root
Password: //empty
Server Choice: MariaDB
Queries: // These are a set of queries to setup the database and add some inventory.
create database squares;
use squares;
create table users(id int not null primary key, username char(30) not null UNIQUE, pass char(30) not
null, credits int);
insert into users(id, username, pass, credits) values(0, 'admin', 'admin', 999999);
create table inventory(id int not null primary key, name char(30) unique, color char(7), price int,
stock int);
insert into inventory(id, name, color, price, stock) values(0, 'White', '#ffffff', 5, 400), (1, 'Black',
'#000000', 5, 400), (2, 'Red', '#ff0000', 8, 250), (3, 'Green', '#00ff00', 8, 250), (4, 'Blue', '#0000ff', 8,
250), (5, 'Grey', '#888888', 8, 250), (6, 'Dark Blue Grey', '#23282d', 25, 8);
create table stock(userid int unique, c0 int, c1 int, c2 int, c3 int, c4 int, c5 int, c6 int);
insert into stock(userid, c0, c1, c2, c3, c4, c5, c6) values(0, 0, 0, 0, 0, 0, 0, 0);
