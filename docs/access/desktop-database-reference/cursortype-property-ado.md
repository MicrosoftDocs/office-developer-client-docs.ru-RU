---
title: Свойство CursorType (ADO)
TOCTitle: CursorType property (ADO)
ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15)
ms:contentKeyID: 48548682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7cdb32bb8ff9bb6e0556a87de0efe82cd919dbe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295186"
---
# <a name="cursortype-property-ado"></a>Свойство CursorType (ADO)


**Область применения**: Access 2013, Office 2013

Указывает тип курсора, используемого в [объекте Recordset.](recordset-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает [значение CursorTypeEnum.](cursortypeenum.md) По умолчанию значение **adOpenForwardOnly**.

## <a name="remarks"></a>Примечания

Используйте свойство **CursorType,** чтобы указать тип курсора, который следует использовать при открытии объекта **Recordset.**

Поддерживается только параметр **adOpenStatic,** если свойство [CursorLocation](cursorlocation-property-ado.md) настроено **на adUseClient.** Если установлено неподтверченные значения, то ошибка не приведет; Вместо этого будет использоваться ближайший поддерживаемый **CursorType.**

Если поставщик не поддерживает запрашиваемого типа курсора, он может вернуть другой тип курсора. Свойство **CursorType** будет изменяться в соответствие с фактическим типом курсора, используемого при открытом объекте [Recordset.](recordset-object-ado.md) Чтобы проверить конкретные функциональные возможности возвращенного курсора, используйте метод [Supports.](supports-method-ado.md) После закрытия **recordset** свойство **CursorType** возвращается к исходному параметру.

На следующей диаграмме показана функциональность поставщика (определена константами метода **Supports),** необходимые для каждого типа курсора.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Для наборов записей этого CursorType</p></th>
<th><p>Метод Supports должен возвращать True для всех этих констант</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>нет</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Хотя **supports****(adUpdateBatch)** может быть верным для динамических и только для курсоров, для пакетных обновлений следует использовать либо набор ключей, либо статический курсор. Установите свойство [LockType](locktype-property-ado.md) **adLockBatchOptimistic** и свойство **CursorLocation** **в adUseClient,** чтобы включить службу Cursor для OLE DB, которая требуется для пакетных обновлений.

Свойство **CursorType** считывалось или записывалось при закрытии **и** только для чтения, когда оно открыто.

**Удаленное использование службы данных** Свойство **CursorType,** используемого на клиентском объекте Recordset, может быть задавано **только adOpenStatic.**

