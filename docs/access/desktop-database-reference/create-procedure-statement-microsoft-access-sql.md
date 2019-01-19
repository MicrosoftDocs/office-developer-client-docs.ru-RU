---
title: Оператор CREATE PROCEDURE (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700768"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>Оператор CREATE PROCEDURE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013 

Создает сохраняемую процедуру.

> [!NOTE]
> Ядро СУБД Access не поддерживает использование оператора CREATE PROCEDURE или любые операторы DDL с базами данных с ядром СУБД Jet, не принадлежащими Microsoft.

## <a name="syntax"></a>Синтаксис

CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement

Оператор CREATE PROCEDURE состоит из трех частей:

|Часть|Описание|
|:---|:----------|
|*procedure*|Название процедуры. Необходимо выполнение стандартных соглашений об именовании.|
|*param1*, *param2*|От 1 до 255 имен полей или параметров. Пример:<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Дополнительные сведения о параметрах см. в разделе [ПАРАМЕТРЫ](parameters-declaration-microsoft-access-sql.md).|
|*datatype*|Один из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимов.|
|*sqlstatement*|Оператор SQL, например SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE и т. д.|


## <a name="remarks"></a>Комментарии

Оператор SQL состоит из выражения PROCEDURE, определяющего имя процедуры, необязательный список определений параметров и одного оператора SQL.

Имя процедуры не может совпадать с именем существующей таблицы.

## <a name="example"></a>Пример

В этом примере присваивается имя запросу EnumFields и выполняется вызов процедуры EnumFields, который вы можете найти в приведенном примере инструкции SELECT.

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
