---
title: Optimize Property--Dynamic (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7276e642e15137bdcfcb939330a3642d96e9a5a2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605179"
---
# <a name="optimize-property--dynamic-ado"></a>Optimize Property--Dynamic (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает, должен быть создан индекс для поля.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

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
