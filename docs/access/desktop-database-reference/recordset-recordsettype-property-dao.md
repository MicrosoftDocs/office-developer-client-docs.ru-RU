---
title: Свойство Recordset.RecordsetType (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307632"
---
# <a name="recordsetrecordsettype-property-dao"></a>Свойство Recordset.RecordsetType (DAO)

**Область применения**: Access 2013, Office 2013

Вы можете использовать **свойство RecordsetType,** чтобы указать, какой набор записей доступен для формы. Чтение и **написание byte**.

## <a name="syntax"></a>Синтаксис

*выражения* . RecordsetType

*выражение*: переменная, представляющая объект **Form**.

## <a name="remarks"></a>Примечания

Свойство **RecordsetType** использует следующие параметры в базе данных Microsoft Access.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Тип recordset</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>Dynaset</p></td>
<td><p>(По умолчанию) Элементы управления связанными могут изменяться на основе одной таблицы или таблиц с отношением один к одному. Для элементов управления, привязанных к полям, основанным на таблицах с отношением один к многим, нельзя изменять данные из поля join с одной стороны связи, если между таблицами не включено каскадное &quot; &quot; обновление.</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>Dynaset (Несовместимые обновления)</p></td>
<td><p>Все таблицы и элементы управления, связанные с их полями, могут быть изменены.</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>Моментальный снимок</p></td>
<td><p>Никакие таблицы или элементы управления, привязанные к их полям, не могут быть изменены.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Если вы не хотите, чтобы данные в связанных средствах управления редактировали, когда форма находится в представлении формы или представлении таблицы данных, можно установить свойство **RecordsetType** до 2.

Свойство **RecordsetType** использует следующие параметры в проекте Microsoft Access (.adp).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Тип recordset</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3</p></td>
<td><p>Моментальный снимок</p></td>
<td><p>Никакие таблицы или элементы управления, привязанные к их полям, не могут быть изменены.</p></td>
</tr>
<tr class="even">
<td><p>4 </p></td>
<td><p>Updatable Snapshot</p></td>
<td><p>(По умолчанию) Все таблицы и элементы управления, связанные с их полями, могут быть изменены.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Изменение свойства **RecordsetType** открытой формы или отчета вызывает автоматическое воссоздание наборов записей.

Формы можно создавать на основе нескольких таблиц с полями, связанными с управлением формами. В зависимости от **параметра свойства RecordsetType** можно ограничить, какие из этих связанных элементов управления можно изменить.

Помимо управления редактированием, предоставляемого **RecordsetType,** каждый контроль формы имеет свойство **Locked,** которое можно задать, чтобы указать, можно ли изменить управление и его данные. Если **заблокированное** свойство за установлено да, изменить данные нельзя.

## <a name="example"></a>Пример

В следующем примере только в том случае, если пользовательский ID является администратором, записи могут обновляться. В этом примере кода свойство **RecordsetType** задает снимок, если общедоступный параметр gstrUserID не является администратором.

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a>См. также

- [Объект Form](https://docs.microsoft.com/office/vba/api/Access.Form)


