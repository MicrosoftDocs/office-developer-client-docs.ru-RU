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

Указывает, следует ли создавать индекс на поле.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Boolean,** которое указывает, следует ли создавать индекс.

## <a name="remarks"></a>Примечания

Индекс может повысить производительность операций, которые находят или сортировать значения в [наборе Recordset.](recordset-object-ado.md) Индекс является внутренним для ADO — вы не можете получить явный доступ или использовать его в приложении.

Чтобы создать индекс в поле, установите свойство Оптимизируйте true **.**  Чтобы удалить индекс, установите это свойство **false**.

**Оптимизация** — это динамическое свойство, [](properties-collection-ado.md) которое примыкает к коллекции свойств объектов [Field,](field-object-ado.md) когда свойство [CursorLocation](cursorlocation-property-ado.md) задано **для adUseClient.**

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
