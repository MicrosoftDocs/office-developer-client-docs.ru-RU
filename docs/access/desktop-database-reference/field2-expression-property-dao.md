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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720088"
---
# <a name="field2expression-property-dao"></a>Свойство Field2.Expression (DAO)

**Применимо к**: Access 2013, Office 2013

Получает или задает выражение, представляющее формулу для вычисляемого поля. Для чтения и записи, **String**.

## <a name="version-information"></a>Сведения о версии

Добавлена версия: Access 2010

## <a name="syntax"></a>Синтаксис

*выражение* . Выражение

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

В Access 2013 можно создавать поля в таблице, вычисление значений. Расчеты могут включать значения из полей в одной таблицы, а также встроенных функций доступа.

Расчет не может содержать поля из таблицы или запросы.

Результаты расчета доступны только для чтения.

## <a name="example"></a>Пример

Следующий пример демонстрирует создание вычисляемого поля. Метод CreateField создает поле с именем **полное имя**. Выражение затем задано значение выражения, вычисляющий значение поля.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

