# Pre Quiz

1. select substr("Oracle World",1,6) from dual;
    - Oracle
2. ABC company wants to give each employee a $100 salary increment. You need to evaluate the results from the EMP table prior to the actual modification. If you do not want to store the results in the database, which statement is valid? 
    - You need to give the arithmetic expression that involves the salary increment in the DISPLAY clause of the SELECT statement. 
3. To display the names of all promos done after January 1, 2001 starting with the latest promo. Which query would give the required result? (Choose all that apply.) 
    - SELECT promo_name,promo_begin_date "START DATE" FROM promotions WHERE promo_begin_date > '01-JAN-01' ORDER BY "START DATE" DESC;
    - SELECT promo_name,promo_begin_date FROM promotions WHERE promo_begin_date > '01-JAN-01' ORDER BY 2 DESC;
4. Which statement is true regarding the default behavior of the ORDER BY clause?
    - In a character sort, the values are case-sensitive.
5. To calculate the number of days from 1st Jan 2007 till date: Dates are stored in the default format of dd-mm-rr. Which SQL statements would give the required output?
    - SELECT SYSDATE - TO_DATE('01/JANUARY/2007') FROM DUAL;, SELECT SYSDATE - TO_DATE('01-JANUARY-2007) FROM DUAL; 
6. To generate a report that shows an increase in the credit  limit by 15% for all customers. Customers whose credit limit has not been entered should have the message "Not Available" displayed. Which SQL statement would produce the required result?
    - SELECT NVL(TO_CHAR(cust_credit_limit*.15),'Not Available') "NEW CREDIT"
FROM customers;
7. The CUSTOMERS table has these columns: CUSTOMER_ID NUMBER(4) NOT NULL; CUSTOMER_NAME VARCHAR2(100) NOT NULL; CUSTOMER_ADDRESS VARCHAR2(150); CUSTOMER_PHONE VARCHAR2(20); You need to produce output that states "Dear Customer customer_name, ". The customer_name data values come from the CUSTOMER_NAME column in the CUSTOMERS table. Which statement produces this output? 
    -  SELECT 'Dear Customer ' || customer_name || ',' FROM customers; 
8. Generate a list of all customer last names with their credit limits from the CUSTOMERS table. Customers who do not have a credit limit should appear last in the list. kindly note that customers who do not have credit card will have NULL against credit limit.Which query would achieve the required result?
    - SELECT cust_last_name,cust_credit_limit FROM customers ORDER BY cust_credit_limit;
9. To display the names of employees that are not assigned to a department. Evaluate this SQL statement: SELECT last_name, first_name FROM employee WHERE dept_id = NULL; .Which change should you make to achieve the desired result? 
    - Change the operator in the WHERE condition.
10. To update the CUST_CREDIT_LIMIT column to NULL for all the customers, where CUST_INCOME_LEVEL has NULL in the CUSTOMERS table. Which SQL statement will accomplish the task? 
    -  UPDATE customers SET cust_credit_limit = NULL WHERE cust_income_level IS NULL;