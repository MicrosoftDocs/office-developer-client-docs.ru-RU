---
title: Инструкция CREATE PROCEDURE (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 2cd84f6e84d35cb24b2fd9b74146f3d401bbaba6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869444"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>Инструкция CREATE PROCEDURE (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013 

Создает хранимую процедуру.

> [!NOTE]
> Ядро базы данных Microsoft Access не поддерживает использование создать процедуру или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Jet.

## <a name="syntax"></a>Синтаксис

ПРОЦЕДУРА СОЗДАНИЯ *процедуры* \[ *тип данных param1*\[, *тип данных param2*\[,... \] \] Как sqlstatement

Инструкция CREATE PROCEDURE состоит из следующих частей:

|Часть|Описание|
|:---|:----------|
|*процедура*|Имя процедуры. Оно должно соответствовать стандартным соглашениям об именах.|
|*param1* *param2*|От одного до 255 имен полей или параметров. Пример:<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>[Дополнительные сведения о параметрах см.](parameters-declaration-microsoft-access-sql.md)|
|*Тип данных*|Одна из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимы.|
|*SQLStatement*|Инструкция SQL, такие как выбор, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE и т.д.|


## <a name="remarks"></a>Замечания

Процедура SQL состоит из предложения PROCEDURE, которое определяет имя процедуры, дополнительный список параметров определения и одной инструкции SQL.

Имя процедуры не может быть имя существующей таблицы.

## <a name="example"></a>Пример

В этом примере имена запроса CategoryList и вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.

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
