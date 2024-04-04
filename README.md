# production solutions

## **Airflow**
___
**The [dag_generate_and_load_data.py](dag_generate_and_load_data.py) waits for the flag from DWH and generates three files in parallel for the CVM Business platform.**

![image](https://github.com/Den-is-me/product_solutions/assets/107809488/5c75840b-cdc1-49b5-a840-888daff09284)
 
 Tools:
*  FileSensor to check the Flag.
*  BranchOperator to check validation of data.
*  PostgresOperator, OracleOperator to isert into or truncate tables and create new files.
*  SSHOperator, BashOperator to execute shell scripts to move files.
*  EmailOperator for alert.

