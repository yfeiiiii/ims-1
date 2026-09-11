CREATE TABLE genres (
    gid INT AUTO_INCREMENT PRIMARY KEY,
    mgenre VARCHAR(50) NOT NULL
);

INSERT INTO genres (mgenre)
VALUES
('Action/Adventure'),
('Comedy'),
('Drama'),
('Fantasy/Sci-Fi');


SELECT * FROM genres;

CREATE TABLE movies (
    mid INT AUTO_INCREMENT PRIMARY KEY,
    mname VARCHAR(100) NOT NULL,
    myear VARCHAR(4) NOT NULL,
    mgenreid INT NOT NULL,
    mrating INT NOT NULL CHECK (mrating BETWEEN 1 AND 5),
    FOREIGN KEY (mgenreid) REFERENCES genres(gid)
);