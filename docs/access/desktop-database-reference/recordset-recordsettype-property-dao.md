---
title: Свойство Recordset. RecordsetType (DAO)
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
# <a name="recordsetrecordsettype-property-dao"></a>Свойство Recordset. RecordsetType (DAO)

**Область применения**: Access 2013, Office 2013

Свойство **RecordsetType** можно использовать, чтобы указать тип набора записей, доступный для формы. **Байт**для чтения и записи.

## <a name="syntax"></a>Синтаксис

*Expression* . RecordsetType

*выражение*: переменная, представляющая объект **Form**.

## <a name="remarks"></a>Замечания

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
<th><p>Тип объекта Recordset</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>нуль</p></td>
<td><p>Типа dynaset</p></td>
<td><p>Умолчани Можно редактировать присвязанные элементы управления на основе одной таблицы или таблиц с отношением "один к одному". Для элементов управления, привязанных к полям, основанным на таблицах с отношением "один ко многим" &quot;, нельзя изменить данные из поля&quot; присоединения на одной стороне отношения, если между таблицами не включено каскадное обновление.</p></td>
</tr>
<tr class="even">
<td><p>1,1</p></td>
<td><p>Динамическое подМножество (несогласованные обновления)</p></td>
<td><p>Можно редактировать все таблицы и элементы управления, привязанные к их полям.</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>Статически</p></td>
<td><p>Не допускается редактирование таблиц и элементов управления, привязанных к их полям.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Если вы не хотите, чтобы данные в привязанных элементах управления были изменены, если форма находится в режиме формы или в режиме таблицы, можно задать для свойства **RecordsetType** значение 2.

Свойство **RecordsetType** использует следующие параметры в проекте Microsoft Access (ADP).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Тип объекта Recordset</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>4</p></td>
<td><p>Статически</p></td>
<td><p>Не допускается редактирование таблиц и элементов управления, привязанных к их полям.</p></td>
</tr>
<tr class="even">
<td><p>SP4</p></td>
<td><p>Обновляемый моментальный снимок</p></td>
<td><p>Умолчани Можно редактировать все таблицы и элементы управления, привязанные к их полям.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Изменение свойства **RecordsetType** для открытой формы или отчета приводит к автоматическому воссозданию объекта Recordset.

Вы можете создавать формы на основе нескольких базовых таблиц с полями, связанными с элементами управления в формах. В зависимости от значения свойства **RecordsetType** можно ограничить возможности редактирования этих связанных элементов управления.

Помимо элемента управления редактирования, предоставленного **RecordsetType**, у каждого элемента управления в форме есть свойство **locked** , которое можно задать, чтобы указать, можно ли редактировать элемент управления и его базовые данные. Если свойству **locked** присвоено значение "Да", данные изменить нельзя.

## <a name="example"></a>Пример

В следующем примере только в том случае, если идентификатор пользователя является АДМИНИСТРАТОРом, могут быть обновлены записи. В этом примере кода для свойства **RecordsetType** задается значение snapshot, если общедоступная переменная гструсерид имеет значение Not admin.

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


