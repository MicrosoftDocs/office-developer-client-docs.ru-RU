---
title: Свойство Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292820"
---
# <a name="field2expression-property-dao"></a>Свойство Field2.Expression (DAO)

**Область применения**: Access 2013, Office 2013

Получает или задает выражение, представляюще формулу для вычисляемой области. Для чтения и записи, **String**.

## <a name="version-information"></a>Сведения о версии

Добавлена версия: Access 2010

## <a name="syntax"></a>Синтаксис

*выражения* . Выражение

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

В Access 2013 можно создать таблицы полей, которые вычисляют значения. Вычисления могут включать значения из полей в одной таблице, а также встроенные функции Access.

Вычисление не может включать поля из других таблиц или запросов.

Результаты вычисления являются только для чтения.

## <a name="example"></a>Пример

В приведенном ниже примере показано, как создать вычисляемое поле. Метод CreateField создает поле с именем **FullName**. Затем для свойства Expression устанавливается выражение, вычисляющее значение поля.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

