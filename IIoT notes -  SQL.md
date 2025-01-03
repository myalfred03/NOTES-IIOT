Workbench MySql:
- Set Workspace
- Set password root
- Verify Status of server, is or isn't running. 

Now Create the Project:

1. Create New Schema
2. Create New Table, this depends on the type of project that you build.
Example the type of columns that you need. 
To storage data Sensor the most simples columns are contain timestamp and data in INT or FLOAT.

**Querys**

**Insert**

 ```
INSERT INTO `training`.`info`
(`id`,
`Name`,
`Age`,
`Country`,
`Height`)
VALUES
(<{id: }>,
<{Name: }>,
<{Age: }>,
<{Country: }>,
<{Height: }>);ç

 ```

 Data Example: 

 ```
INSERT INTO `training`.`info`
(`id`,
`Name`,
`Age`,
`Country`,
`Height`)
VALUES
(1,
"Yesser",
29,
"Nicaragua",
185);
 ```

 **SELECT**

 ```
SELECT * FROM training.info where id= 2;

SELECT * FROM training.info where Country = "Nicaragua";

SELECT * FROM training.info where Age > 20;
 ```