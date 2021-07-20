## 대소문자는 큰 상관이 없다. 
## Select 
  SELECT column1, column2    
  FROM table_name;   
  -> table_name 테이블에서 column1과 2에 대한 값을 불러와라   
  
  SELECT * FROM table_name; -> table_name 에 있는 모든 값들을 불러와라.  
  
  ### DISTINCT
  SELECT DISTINT column1, column2    
  FROM table_name; -> 중복되는 값이 없이    
  
  SELECT COUNT(DISTINCT Country) FROM Customers; -> 중복되지 않은 것들의 개수  
  
## WHERE -조건문 같은 느낌이다. 
  SELECT * FROM Customers.   
  WHERE Country = 'MEXICO'; -> 나라가 멕시코인 데이터만 표현이된다. 
  
  <>  -> 같지 않으면    
  BETWEEN a and b -> a,b 사이에 있으면 (a,b 모두 포함)     
  LIKE 's%' ->s로 시작하는 단어이면 이런 느낌    
  City IN ('Paris','London'); 여기 안에 있으면  
## AND OR NOT 은 c와 비슷하다. 
## ORDER BY 
  SELECT column1, column2   
  FROM table_name   
  ORDER BY column1, column2  ASC|DESC; -> 커지게 하거나 작아지게 설정 가능
     
  SELECT * FROM Customers   
  ORDER BY Country, CustomerName; -> 먼저는 나라에 대한 정렬을 하고 같다면 이름에 관한 정렬을 한다.   
  
  SELECT * FROM Customers   
  ORDER BY COUNTRY ASC, CustomerName DESC; ->이런식으로 기준을 다르게 할 수도 있다.   
## INSERT INTO -> 데이터를 추가할 수 있다. 
  INSERT INTO table_name (column1, column2, column3, ...)   
  VALUES (value1, value2, value3, ...);  -> 추가할 columd의 이름과 값을 넣을 수 있다. 
  모든 곳에 값을 넣지 않으면 남은 곳은 null이 들어가게 된다. 
  
  INSERT INTO table_name   
  VALUES (value1, value2, value3, ...); -> 모든 colum 의 값을 추가한다면 값만 순서대로 적으면 된다.    
## NULL
  연산자로 NULL 파악 불가   
  IS NULL이나 IS NOT NULL 사용해야 함 
  
# UPDATE와 DELETE WHERE 안 빠트리기  
## UPDATE-SET
  UPDATE table_name   
  SET column1 = value1, column2 = value2, ...   
  WHERE condition;   -> WHERE 부분을 빠트린다면 모든 곳들이 바뀌게 된다.   
  
## DELETE
  DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';   
  DELETE FROM table_name; ->모든 데이터를 지운다. 테이블은 지우지 않는다. 
  
  
## LIMIT 
  SELECT * FROM Customers LIMIT 3; ->데이터를 세개만 보여준다. 
  
  SELECT * FROM Customers   
  WHERE Country='Germany'   
  LIMIT 3;   -> where 을 추가해 원하는 것만 보여주는 것도 가능하다. 

## MIN() MAX()
  SELECT MIN(column_name)   
  FROM table_name   
  WHERE condition;   
  
  SELECT MIN(Price) AS SmallestPrice   
  FROM Products; -> 뒤에 as 는 MIN(price)를 SmallestPrice로 표현한다. 
  
  
  
  
