# WEB2040_the_courses_tables
The "courses" table, for database examples and quizzes

```sql
CREATE TABLE `courses` (
	`id` int(11) NOT NULL,
	`code` char(7) NOT NULL,
	`name` varchar(30) NOT NULL,
	`description` varchar(100) NOT NULL,
	`start_date` date NOT NULL,
	`end_date` date DEFAULT NULL,
	`professor` varchar(50) NOT NULL,
	`start_time` time NOT NULL,
	`cost` float NOT NULL,
	`credit_hours` int(2) NOT NULL,
	`prerequisites` varchar(87) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

ALTER TABLE `courses` ADD PRIMARY KEY (`id`), ADD UNIQUE KEY `code` (`code`);
ALTER TABLE `courses` MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=23;

INSERT INTO `courses` (`code`, `name`, `description`, `start_date`, `end_date`, `professor`, `start_time`, `cost`, `credit_hours`, `prerequisites`) VALUES
('WEB3000', 'Agile and TDD (QA/Test)', 'Agile and TDD (QA/Test)', '2018-07-24', '2019-04-24', 'Salvi Pascual', '05:30:00', 500, 2, 'ROR1000,WEB2910,WEB2900,WEB2040,WEB2020'),
('WEB2910', 'Modern MV* Back End Frameworks', 'Modern MV* Back End Frameworks', '2018-07-11', '2019-04-11', 'frank', '05:40:00', 550, 2, 'ROR1000;WEB2910;WEB2020;WEB2000;COP100'),
('WEB2020', 'Intermediate Styling Technique', 'Advance CSS', '2018-08-16', '2018-09-30', 'Salvi Pascual', '05:30:00', 5000, 4, 'WEB1010;WEB1100;WEB2000'),
('WEB2900', 'Modern MV Front End Frameworks', 'PHP language', '2018-09-16', '2018-10-30', 'Jeme Rahman', '05:30:00', 7000, 6, 'WEB1010;WEB1100;WEB2000;WEB2040'),
('WEB2000', 'Intermediate Front End Structu', 'Intermediate Front End Structure', '2018-08-01', '2018-08-22', 'Frank Veloz Montero', '05:30:00', 500, 2, 'WEB1010;WEB1100'),
('WEB2040', 'SQL Databases', 'SQL Databases', '2018-08-25', '2018-09-22', 'Salvi Pascual', '05:30:00', 500, 2, 'WEB1010;WEB1100'),
('WEB1010', 'Basic Front-End Programming', 'JS,HTML5,CSS', '2018-04-27', '2020-12-31', 'McMiller, Troy', '15:00:00', 200, 2, 'High School Diploma or GED'),
('WEB1100', 'Basic Front-End Promrmming II', 'JSON,ES6, NODE.JS NPM, JQUERY', '2019-04-27', '0000-00-00', 'Brown, Pablo', '15:00:00', 20, 99, 'WEB1010'),
('CAP2000', 'Hat making', 'make hats all day', '2019-04-27', '2030-12-31', 'McMiller, Troy', '13:00:00', 20, 1, 'Masters Degree'),
('ROR1000', 'Hunt and survive in the jungle', 'Hunt, and Survive', '2023-04-27', '2025-12-31', 'Stalin, Joseph', '00:00:00', 200, 50, 'WEB1100');
```
