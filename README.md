# Week5
**要求三**
```
INSERT INTO member(name, username, password, follower_count) VALUES('Ohtani Showyu','test','test',100);
INSERT INTO member(name, username, password, follower_count) VALUES('John','test1','test1',15);
INSERT INTO member(name, username, password, follower_count) VALUES('Mayer','test2','test2',10);
INSERT INTO member(name, username, password, follower_count) VALUES('Jimmy','test3','test3',50);
INSERT INTO member(name, username, password, follower_count) VALUES('Louis','test4','test4',70);
```
```
SELECT * FROM member;
```
![image](https://github.com/siouyu/Week5/blob/main/img/3_selectAll.png)
```
SELECT * FROM member ORDER BY time desc;
```
![image](https://github.com/siouyu/Week5/blob/main/img/3_selectByTime.png)
```
SELECT * FROM member ORDER BY  time desc LIMIT 1,3;
```
![image](https://github.com/siouyu/Week5/blob/main/img/3_select2-4.png)
```
SELECT * FROM member WHERE username='test';
```
![image](https://github.com/siouyu/Week5/blob/main/img/3_selectTest.png)
```
SELECT * FROM member WHERE username='test' and password='test';
```
![image](https://github.com/siouyu/Week5/blob/main/img/3_selectBothTest.png)
```
SET SQL_SAFE_UPDATES=0;
UPDATE member SET name='test2' WHERE username='test';
```
![image](https://github.com/siouyu/Week5/blob/main/img/3_update.png)

**要求四**
```
SELECT COUNT(*) FROM member;
```
![image](https://github.com/siouyu/Week5/blob/main/img/4_all.png)
```
SELECT SUM(follower_count) FROM member;
```
![image](https://github.com/siouyu/Week5/blob/main/img/4_sum.png)
```
SELECT AVG(follower_count) FROM member;
```
![image](https://github.com/siouyu/Week5/blob/main/img/4_avg.png)

**要求五**
```
SELECT member.name, message.content FROM member INNER JOIN message ON member.id=message.member_id;
```
![image](https://github.com/siouyu/Week5/blob/main/img/5_all.png)
```
SELECT member.name, message.content FROM member INNER JOIN message ON member.id=message.member_id WHERE username='test';
```
![image](https://github.com/siouyu/Week5/blob/main/img/5_test.png)
```
SELECT AVG(like_count) FROM member INNER JOIN message ON member.id=message.member_id WHERE username='test';
```
![image](https://github.com/siouyu/Week5/blob/main/img/5_avg.png)
