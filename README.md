CREATE DATABASE reservation_system;

USE reservation_system;

CREATE TABLE users (
    username VARCHAR(50) PRIMARY KEY,
    password VARCHAR(50) NOT NULL
);

INSERT INTO users VALUES ('admin', '1234');

CREATE TABLE trains (
    train_number INT PRIMARY KEY,
    train_name VARCHAR(100) NOT NULL
);

INSERT INTO trains VALUES
(12345, 'Rajdhani Express'),
(12346, 'Shatabdi Express'),
(12347, 'Vande Bharat Express'),
(12348, 'Gorakhpur Express');

CREATE TABLE reservations (
    pnr BIGINT PRIMARY KEY,
    passenger_name VARCHAR(100) NOT NULL,
    train_number INT NOT NULL,
    train_name VARCHAR(100) NOT NULL,
    class_type VARCHAR(30) NOT NULL,
    journey_date DATE NOT NULL,
    source_station VARCHAR(100) NOT NULL,
    destination_station VARCHAR(100) NOT NULL
);
