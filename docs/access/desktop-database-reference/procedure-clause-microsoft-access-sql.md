---
title: Предложение PROCEDURE (Microsoft Access SQL)
TOCTitle: PROCEDURE clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 72f31c71e710cca79695a7221f0e033d18d2f420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301381"
---
# <a name="procedure-clause-microsoft-access-sql"></a>Предложение PROCEDURE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Определяет имя и необязательные параметры для запроса.

> [!NOTE]
> Предложение PROCEDURE было замехано заявлением PROCEDURE. Хотя предложение PROCEDURE по-прежнему поддерживается, заявление PROCEDURE предоставляет более набор возможностей предложения PROCEDURE и является рекомендуемой синтаксис.

## <a name="syntax"></a>Синтаксис

ИМЯ  \[ *ПРОЦЕДУРы param1 datatype,* \[ *param2 datatype*, \[ ...\]\]

Предложение PROCEDURE имеет указанные здесь части.

|Часть |Описание |
|:----|:-----------|
|*name* |Название процедуры. Необходимо выполнение стандартных соглашений об именовании.|
|*param1*, *param2* |Одно или несколько имен полей или параметров. Например:<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Дополнительные сведения о параметрах см. [в параметрах.](parameters-declaration-microsoft-access-sql.md)|
|*datatype* | Один из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимов. |


## <a name="remarks"></a>Примечания

Процедура SQL состоит из предложения PROCEDURE (которое указывает имя процедуры), необязательного списка определений параметров и одного SQL процедуры. Например, процедура получения номера части может выполнить запрос, который \_ \_ извлекает указанный номер части.

> [!NOTE]
> - Если предложение содержит несколько определений полей (то есть пары *param-datatype),* разделяйте их запятой.
> - За предложением PROCEDURE следует SQL (например, [SELECT](select-statement-microsoft-access-sql.md) или [UPDATE).](update-statement-microsoft-access-sql.md)

## <a name="example"></a>Пример

В этом примере присваивается имя запросу CategoryList и выполняется вызов процедуры EnumFields, которую вы можете найти в приведенном примере для оператора SELECT.

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
