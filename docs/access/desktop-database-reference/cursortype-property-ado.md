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

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [CursorTypeEnum.](cursortypeenum.md) Значение по умолчанию **— adOpenForwardOnly.**

## <a name="remarks"></a>Заметки

Используйте свойство **CursorType,** чтобы указать тип курсора, который должен использоваться при открытии **объекта Recordset.**

Поддерживается только **параметр adOpenStatic,** если свойство [CursorLocation](cursorlocation-property-ado.md) имеет свойство **adUseClient.** Если установлено неподтверченные значения, ошибка не будет создана; Вместо него будет использоваться **ближайший поддерживаемый cursorType.**

Если поставщик не поддерживает запрашиваемого типа курсора, он может вернуть другой тип курсора. Свойство **CursorType** будет изменяться в соответствие с фактическим типом курсора, который используется при открытом объекте [Recordset.](recordset-object-ado.md) Чтобы проверить конкретные функции возвращенного курсора, используйте метод [Supports.](supports-method-ado.md) После закрытия объекта **Recordset** свойство **CursorType** возвращается к исходному параметру.

На следующей диаграмме показаны функции поставщика (которые определены константами метода **Supports),** необходимые для каждого типа курсора.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Для recordset этого CursorType</p></th>
<th><p>Метод Supports должен возвращать true для всех этих констант</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>Нет</p></td>
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
> Хотя **supports****(adUpdateBatch)** может иметь значение true для динамических курсоров и курсоров только вперед, для пакетных обновлений следует использовать либо набор ключей, либо статический курсор. Установите для свойства [LockType](locktype-property-ado.md) свойство **adLockBatchOptimistic,** а для **свойства CursorLocation** — **adUseClient,** чтобы включить службу курсора для OLE DB, которая требуется для пакетных обновлений.

Свойство **CursorType** считывалось и записывалось при закрытии объекта **Recordset** и только для чтения при его открытом режиме.

**Использование удаленной службы данных** При клиентском объекте Recordset свойство **CursorType** можно установить только в **adOpenStatic.**

