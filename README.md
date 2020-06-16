# DB_relationship_exercise

## Create table

### Create Users table
```
CREATE TABLE users (
    	id int NOT NULL AUTO_INCREMENT PRIMARY KEY,
	email VARCHAR(50),
	password VARCHAR(50),
	role VARCHAR(50),
	created_at DATETIME,
	updated_at DATETIME     
);
```
### Create categories table 
```
CREATE TABLE categories(
	id int NOT NULL AUTO_INCREMENT PRIMARY KEY,
	name VARCHAR(50),
	created_at DATETIME,
	updated_at DATETIME 
);
```
### Create photos table
```
CREATE TABLE photos(
	id int NOT NULL AUTO_INCREMENT PRIMARY KEY,
	title VARCHAR(100),
	category_id INT,
	image VARCHAR(100),
	created_at DATETIME,
	updated_at DATETIME,
	FOREIGN KEY (category_id) REFERENCES categories(id)
);
```
### Create tags table
```
CREATE TABLE tags(
	id int NOT NULL AUTO_INCREMENT PRIMARY KEY,
	name VARCHAR(50),
	created_at DATETIME,
	updated_at DATETIME 
);
```
### Create taggable table
```
CREATE TABLE taggale(
	tag_id int,
    	photo_id int,
	created_at DATETIME,
	updated_at DATETIME,
	FOREIGN KEY (tag_id) REFERENCES tags(id),
    	FOREIGN KEY (photo_id) REFERENCES photos(id),
  	PRIMARY KEY (tag_id,photo_id)
);
```
### Create photo_descriptions table
```
CREATE TABLE photo_descriptions(
	id int NOT NULL,
	content VARCHAR(50),
	created_at DATETIME,
	updated_at DATETIME,
	FOREIGN KEY (id) REFERENCES photos(id),
	PRIMARY KEY (id)
);
```
## Insert into database
### Users
```

```
```

