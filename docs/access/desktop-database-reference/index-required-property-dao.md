---
title: Свойство Index.Required (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703134"
---
# <a name="indexrequired-property-dao"></a>Свойство Index.Required (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, требуется ли объект **[поля](field-object-dao.md)** ненулевое значение.

## <a name="syntax"></a>Синтаксис

*выражение* . Обязательно

*выражение* Переменная, которая представляет объект **индекса** .

## <a name="remarks"></a>Замечания

> [!NOTE]
> При установке этого свойства для объекта **индекса** или объекта **поля** задайте его для объекта **поля** . Перед, объект **индекса** проверять правильность настройки свойства для объекта **поля** .

Доступность свойства **необходимые** зависит от объекта, который содержит коллекцию [полей](fields-collection-dao.md) , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если принадлежит коллекции полей</p></th>
<th><p>Затем необходимо — это</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>индекса</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>набора записей</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Отношения</strong> объектов</p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>

