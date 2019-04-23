---
title: Оптимизация динамического свойства (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bb7872514a828fdd97fb404f5366c35ff9a883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288254"
---
# <a name="optimize-dynamic-property-ado"></a>Оптимизация динамического свойства (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, следует ли создать индекс для поля.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **логическое** значение, которое указывает, следует ли создать индекс.

## <a name="remarks"></a>Замечания

Индекс может увеличить производительность операций, в которых выполняется поиск или сортировка значений в [наборе записей](recordset-object-ado.md). Индекс является внутренним по отношению к ADO, поэтому вы не можете явно получить доступ к нему или использовать его в вашем приложении.

Чтобы создать индекс для поля, задайте для свойства **optimize** значение **true**. Чтобы удалить индекс, установите для этого свойства **значение false**.

**Optimize** — это динамическое свойство, добавленное в коллекцию [свойств](properties-collection-ado.md) объекта [поля](field-object-ado.md) , если для свойства [CursorLocation](cursorlocation-property-ado.md) задано значение **адусеклиент**.

**Usage**

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
