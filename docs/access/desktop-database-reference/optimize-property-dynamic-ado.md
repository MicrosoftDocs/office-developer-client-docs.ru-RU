---
title: Оптимизация свойство--динамической (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62af17d9590b2fad39d61639a32de536f0438193
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883234"
---
# <a name="optimize-property--dynamic-ado"></a>Оптимизация свойство--динамической (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает, должен быть создан индекс для поля.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Boolean** , которое указывает, должен быть создан индекс.

## <a name="remarks"></a>Замечания

Индекс можно повысить производительность операций, поиск или отсортировать значения в [набор записей](recordset-object-ado.md). Индекс является внутренним в ADO — явно не удается получить доступ к или использовать в приложении.

Чтобы создать индекс для поля, присвойте свойству **оптимизировать** значение **True**. Чтобы удалить индекс, этому свойству присвоено значение **False**.

**Оптимизировать** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта [поля](field-object-ado.md) при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.

**Использование**

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
