---
title: Field2.Expression Property (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f3cbb7ca4078fb92ad721d85679dabee9237f85
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481967"
---
# <a name="field2expression-property-dao"></a>Field2.Expression Property (DAO)

**Применимо к**: Access 2013 | Office 2013

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

