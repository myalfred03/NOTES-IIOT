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
 
SELECT Avg(Age) As `Average age` FROM training.info;

SELECT * FROM training.info ORDER by Name Desc;
 ```

**Update**

```

UPDATE `training`.`info` SET `Name` = "Alfred" WHERE `id` = 2;

UPDATE `training`.`info` SET `Age` = 30 WHERE `id` = 2;

Select * From `training`.`info`;

``` 

**Delete**

```
DELETE From training.info where id=2;

DELETE From training.info; "Be careful, you can erase all data"
```
Learn more querys

` https://www.w3schools.com/sql/default.asp`

**Insert From Form to Mysql**

```
var id = msg.payload.id;
var name = msg.payload.Name;
var age = msg.payload.Age;
var country = msg.payload.Country;
var height = msg.payload.Height;



msg.topic = ' INSERT INTO`training`.`info` (`id`,`Name`, `Age`, `Country`, `Height`) VALUES ('+id+', "'+name+'",  '+age+', "'+country+'", '+height+'); ';
return msg;
```

**Select to show in a table custom HTML**

```
<html>

<head> 
    <style>
        #history {
            th,
            td border: 1px solid black;
            border-collapse: collapse;
            font-family: "Arial";
            width: 100%;
            
        }

        #history td,
        #history th {
            border: 1px solid #000000;
            padding: 8px;
            
        }

        #history tr:nth-child(even) {
            background-color: #ffffff;
        }

        #history tr:hover {
            background-color: #73E0FD;
        }

        #history th {
            padding-top: 12px;
            padding-bottom: 12px;
            text-align: center;
            background-color: #A8E7FC;
            color: black;
        }


    </style>
    
    </head>

<body>
    <table id= "history" border="1">
         <tr align="center">
             <th>id</th>
              <th>Name</th>
               <th>Age</th>
                </tr>
                 <tbody>
                     <tr align="center" ng-repeat="row in msg.payload">
                         <td ng-repeat="item in row"> {{item}} </td>
                          </tr>
                </tbody>
        </table>
```


## Data flow
```mermaid
graph LR
A[Random/PLC values] --Write--> B[MySQL] --Read--> C[Node-RED Chart] 
```