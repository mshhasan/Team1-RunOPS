#Database connection problem guide

##Symptoms
- User cannot access database
- User denied specific action

##Quick Checks
1) Check user login not disabled
	```sql
	SELECT * FROM dbo.syslogins WHERE login = N''	
	```
2) Check password correct
3) Check database user not orphaned
	```sql
	SELECT * FROM dbo.syslogins l
		LEFT JOIN dbo.sysusers u
		on l.name = u.loginname
	WHERE login = N''	
	```
