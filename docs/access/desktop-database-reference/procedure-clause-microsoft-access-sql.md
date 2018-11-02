---
title: Предложение ПРОЦЕДУРЫ (Microsoft Access SQL)
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
ms.openlocfilehash: dd99fb241572f2e16eae914ba7d1dea31e1d097f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924262"
---
# <a name="procedure-clause-microsoft-access-sql"></a>Предложение ПРОЦЕДУРЫ (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Определяет имя и необязательные параметры для запроса.

> [!NOTE]
> Предложение ПРОЦЕДУРЫ, был заменен на оператор ПРОЦЕДУРЫ. Несмотря на то, что предложение ПРОЦЕДУРЫ по-прежнему поддерживается, оператор ПРОЦЕДУРЫ обеспечивает подмножеством возможность предложение ПРОЦЕДУРЫ и рекомендуемые синтаксис.

## <a name="syntax"></a>Синтаксис

ПРОЦЕДУРЫ *имя* \[ *тип данных param1*\[, *тип данных param2*\[,...\]\]

Предложение процедура состоит из следующих частей:

|Часть |Описание |
|:----|:-----------|
|*name* |Имя процедуры. Оно должно соответствовать стандартным соглашениям об именах.|
|*param1* *param2* |Один или несколько имен полей или параметров. Пример:<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>[Дополнительные сведения о параметрах см.](parameters-declaration-microsoft-access-sql.md)|
|*Тип данных* | Одна из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимы. |


## <a name="remarks"></a>Примечания

Процедура SQL состоит из предложения PROCEDURE (определяющего имя процедуры), дополнительный список параметров определения и одной инструкции SQL. Например, процедура Get\_часть\_номер может выполнять запрос, который извлекает указанную часть номер.

> [!NOTE]
> - Если предложение включает более одного определения поля (то есть, пары *параметр-тип данных* ), разделяйте их запятыми.
> - Предложение процедуру необходимо следовать инструкции SQL [(например, [ВЫБЕРИТЕ](select-statement-microsoft-access-sql.md) инструкции)](update-statement-microsoft-access-sql.md) .

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
