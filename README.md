CREATE TABLE STUDENT(USN CHAR(10),
     SNAME VARCHAR(20),
    ADDRESS VARCHAR(25),
    PHONE NUMBER(10),
    GENDER CHAR,
    CONSTRAINT A PRIMARY KEY(USN)
     );
     
     CREATE TABLE SEMSEC(SSID CHAR(2),
    SEM NUMBER(1),
    SEC CHAR,
   CONSTRAINT B PRIMARY KEY(SSID),
   CONSTRAINT C CHECK(SEM BETWEEN 1 AND 8)
   );
   
   CREATE TABLE CLASS(USN CHAR(10),
      SSID CHAR(2),
      CONSTRAINT D PRIMARY KEY(USN,SSID),
      CONSTRAINT E FOREIGN KEY(USN) REFERENCES STUDENT(USN) ON DELETE CASCADE,
      CONSTRAINT F FOREIGN KEY(SSID) REFERENCES SEMSEC(SSID) ON DELETE CASCADE
      );
      
      CREATE TABLE SUBJECT(SUBCODE VARCHAR(7),
    TITLE VARCHAR(20),
   SEM NUMBER(1),
   CREDITS NUMBER(1),
    CONSTRAINT G PRIMARY KEY(SUBCODE)
   );
   
   CREATE TABLE IAMARKS(USN CHAR(10),
     SUBCODE VARCHAR(7),
     SSID CHAR(2),
     TEST1 NUMBER(2),
     TEST2 NUMBER(2),
     TEST3 NUMBER(2),
     FINALIA NUMBER(2),
    CONSTRAINT H PRIMARY KEY(USN,SUBCODE,SSID),
    CONSTRAINT I FOREIGN KEY(USN) REFERENCES STUDENT(USN) ON DELETE CASCADE,
    CONSTRAINT J FOREIGN KEY(SSID) REFERENCES SEMSEC(SSID) ON DELETE CASCADE,         CONSTRAINT K FOREIGN KEY(SUBCODE) REFERENCES SUBJECT(SUBCODE) ON DELETE        CASCADE
   );
   
   
   
   USN            SNAME            ADDRESS         PHONE        GENDER
----------    ----------------  ------------    ----------   ---------- -
1MV17CS001     AASHISH          BANGALORE       1020304050   M
1MV17CS060      NAELA           MYSORE          1122334455   F
1MV17CS130     MILIND           JAMMU           5060708090   M
1MV16CS001     ABHIJITH         PUNE            9988776655   M
1MV16CS060      NIKITHA         HYDERABAD       9080706050   F
1MV16CS130      SANJANA         GUWAHATTI       1234567890   F
1MV15CS001     ANSHUMAN         PANAJI          1112223334   M 
1MV15CS060      AMRUTHA         BANGALORE       1002003004   F
1MV15CS130      BHUVANESH       JAIPUR          9008007006   M
1MV14CS001      DEVAYANI        BANGALORE       10020030     F
1MV14CS060      DAVID           KOCHI           90080070     M
1MV14CS130      AISHWARYA       MUMBAI          1000020000   F




    INSERT INTO STUDENT VALUES('1MV17CS001','AASHISH','BANGALORE',1020304050,'M')
    Enter value for usn: 1MV17CS060
Enter value for sname: NAELA
Enter value for address: MYSORE
Enter value for phone: 1122334455
Enter value for gender: F
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV17CS060','NAELA','MYSORE',1122334455,'F')

Enter value for usn: 1MV17CS130
Enter value for sname: MILIND
Enter value for address: JAMMU
Enter value for phone: 5060708090
Enter value for gender: M
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV17CS130','MILIND','JAMMU',5060708090,'M')

Enter value for usn: 1MV16CS001
Enter value for sname: ABHIJITH
Enter value for address: PUNE
Enter value for phone: 9988776655
Enter value for gender: M
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV16CS001','ABHIJITH','PUNE',9988776655,'M')

Enter value for usn: 1MV16CS060
Enter value for sname: NIKITHA
Enter value for address: HYDERABAD
Enter value for phone: 9080706050
Enter value for gender: F
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV16CS060','NIKITHA','HYDERABAD',9080706050,'F')


Enter value for usn: 1MV16CS130
Enter value for sname: SANJANA
Enter value for address: GUWAHATTI
Enter value for phone: 1234567890
Enter value for gender: F
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV16CS130','SANJANA','GUWAHATTI',1234567890,'F')

Enter value for usn: 1MV15CS001
Enter value for sname: ANSHUMAN
Enter value for address: PANAJI
Enter value for phone: 1112223334
Enter value for gender: M
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV15CS001','ANSHUMAN','PANAJI',1112223334,'M')

Enter value for usn: 1MV15CS060
Enter value for sname: AMRUTHA
Enter value for address: BANGALORE
Enter value for phone: 1002003004
Enter value for gender: F
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV15CS060','AMRUTHA','BANGALORE',1002003004,'F')

Enter value for usn: 1MV15CS130
Enter value for sname: BHUVANESH
Enter value for address: JAIPUR
Enter value for phone: 9008007006
Enter value for gender: M
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV15CS130','BHUVANESH','JAIPUR',9008007006,'M')

Enter value for usn: 1MV14CS001
Enter value for sname: DEVAYANI
Enter value for address: BANGALORE
Enter value for phone: 10020030
Enter value for gender: F
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV14CS001','DEVAYANI','BANGALORE',10020030,'F')

Enter value for usn: 1MV14CS060
Enter value for sname: DAVID
Enter value for address: KOCHI
Enter value for phone: 90080070
Enter value for gender: M
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV14CS060','DAVID','KOCHI',90080070,'M')


Enter value for usn: 1MV14CS130
Enter value for sname: AISHWARYA
Enter value for address: MUMBAI
Enter value for phone: 1000020000
Enter value for gender: F
old   1: INSERT INTO STUDENT VALUES('&USN','&SNAME','&ADDRESS',&PHONE,'&GENDER')
new   1: INSERT INTO STUDENT VALUES('1MV14CS130','AISHWARYA','MUMBAI',1000020000,'F')


SSID        SEM          SEC
--         ----         ----- -
2A           2            A
2B           2            B
2C           2            C
4A           4            A
4B           4            B
4C           4            C 
6A          6             A
6B          6             B
6C          6             C
8A          8             A
8B          8             B
8C          8             C

USN         SSID
-------     -----
1MV14CS001   8A
1MV14CS060   8B
1MV14CS130   8C
1MV15CS001   6A
1MV15CS060   6B
1MV15CS130   6C
1MV16CS001   4A
1MV16CS060   4B
1MV16CS130   4C
1MV17CS001   2A
1MV17CS060   2B
1MV17CS130   2C

USN          SUBCODE   SSID   TEST1   TEST2     TEST3    FINALIA
----------   -------   --     -----   -----     ----------
1MV17CS001   15CS21    2A     15      14        13
1MV17CS060   15PCD23   2B     15      15        14
1MV17CS130   15CS21    2C     11      12        13
1MV16CS001   15CS42    4A     19      19        18
1MV16CS060   15CS44    4B     5       8         5
1MV16CS130   15CS42    4C     20      20        20
1MV15CS001   15CS64    6A     12      12        12
1MV15CS060   15CS62    6B     18      19        20
1MV15CS130   15CS64    6C     8       12        11
1MV14CS001   10CS81    8A     3       11          12
1MV14CS060   10CS842   8B     0       0         7
1MV14CS130   10CS81    8C     0       0         20

SELECT S.USN,S.SNAME,S.ADDRESS,S.PHONE,S.GENDER
 FROM STUDENT S,CLASS C,SEM_SEC SS
 WHERE S.USN=C.USN AND  
                SS.SSID=C.SSID  AND
                SS.SEM=4 AND
                SS.SEC='C';
                
                
                SELECT SS.SEM,SS.SEC,S.GENDER,COUNT(S.GENDER)
  FROM STUDENT S,SEMSEC SS,CLASS C
  WHERE S.USN=C.USN  AND  SS.SSID=C.SSID 
  GROUP BY SS.SEM,SS.SEC,S.GENDER;
  
  
  CREATE VIEW TEST1_MARKS AS
 SELECT USN,SUBCODE,TEST1
 FROM IAMARKS
 WHERE USN='1MV15CS060';
 
 
 
 UPDATE IAMARKS SET TEST1=19,TEST2=18,TEST3=17 WHERE USN='1MV14CS001';
 UPDATE IAMARKS SET TEST1=11,TEST2=0,TEST3=14 WHERE USN='1MV14CS060';
 UPDATE IAMARKS SET TEST1=10,TEST2=0,TEST3=7 WHERE USN='1MV14CS130';
 SELECT * FROM IAMARKS;
 USN         SUBCODE   SSID  TEST1      TEST2      TEST3  FINALIA
----------  -------  --     ----  ------------   -------
1MV17CS001   15CS21    2A   15         14         13
1MV17CS060   15PCD23   2B   15         15         14
1MV17CS130   15CS21    2C   11         12         13
1MV16CS001   15CS42    4A   19         19         18
1MV16CS060   15CS44    4B   5          8          5
1MV16CS130   15CS42    4C   20         20         20
1MV15CS001   15CS64    6A   12         12         12
1MV15CS060   15CS62    6B   18         19         20
1MV15CS130   15CS64    6C   8          12         11
1MV14CS001   10CS81    8A   19         18         17    
1MV14CS060   10CS842   8B   11         0          14
1MV14CS130   10CS81    8C   10         0          7


CREATE OR REPLACE PROCEDURE AVGMARKS
    IS
   CURSOR C_IAMARKS IS
   SELECT GREATEST(TEST1,TEST2) AS A,GREATEST(TEST1,TEST3) AS B,GREATEST(TEST2,TEST3) AS C
   FROM IAMARKS
   WHERE FINALIA IS NULL
    FOR UPDATE;
    C_A NUMBER;
    C_B NUMBER;
   C_C NUMBER;
   C_SUM NUMBER;
   C_AVG NUMBER;
   BEGIN
   OPEN C_IAMARKS;
   LOOP
   FETCH C_IAMARKS INTO C_A,C_B,C_C;
   EXIT WHEN C_IAMARKS%NOTFOUND;
   DBMS_OUTPUT.PUT_LINE(C_A||''||C_B||''||C_C);
   IF(C_A!=C_B) THEN
   C_SUM:=C_A+C_B;
   ELSE
   C_SUM:=C_A+C_C;
   END IF;
   C_AVG:=C_SUM/2;
   DBMS_OUTPUT.PUT_LINE('SUM='||C_SUM);
   DBMS_OUTPUT.PUT_LINE('AVERAGE='||C_AVG);
   UPDATE IAMARKS SET FINALIA=C_AVG
   WHERE CURRENT OF C_IAMARKS;
   END LOOP;
   CLOSE C_IAMARKS;
   END;
   
   
   UPDATE IAMARKS SET FINALIA=NULL;
   
   SELECT S.USN,S.SNAME,S.ADDRESS,S.PHONE,S.GENDER,
    ( CASE 
    WHEN IA.FINALIA BETWEEN 17 AND 20
    THEN 'OUTSTANDING'
    WHEN IA.FINALIA BETWEEN 12 AND 16
    THEN 'AVERAGE'
    ELSE 'WEAK'
    END
    ) AS CAT
   FROM STUDENT S,SEMSEC SS,IAMARKS IA
   WHERE S.USN=IA.USN AND
   SS.SSID=IA.SSID AND
   SS.SEM=8;
   
