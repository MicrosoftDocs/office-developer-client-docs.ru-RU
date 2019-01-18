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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700761"
---
# <a name="cursortype-property-ado"></a>Свойство CursorType (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает тип курсора, используемого в объекте [набора записей](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [CursorTypeEnum](cursortypeenum.md) . Значение по умолчанию — **adOpenForwardOnly**.

## <a name="remarks"></a>Замечания

Свойство **CursorType** определяет тип указателя, который должен использоваться при открытии объекта **набора записей** .

Только параметр **adOpenStatic** поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет значение **adUseClient**. Если задано значение не поддерживается, сообщение об ошибке не приведет к; ближайший поддерживаемый **CursorType** будет использоваться.

Если поставщик поддерживает курсором запрошенного типа, он может вернуть курсор другого типа. Свойство **CursorType** изменится в соответствии в используемый тип фактический курсора при открытом объекта [набора записей](recordset-object-ado.md) . Проверка определенных функций возвращенные курсора, используйте метод [поддерживает](supports-method-ado.md) . После закрытия **набора записей**свойство **CursorType** возвращается в исходное значение.

В приведенной ниже диаграмме показано функциональности поставщика (обозначенный **поддерживает** метод константы) требуется для каждого типа курсора.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Для набора записей в этом CursorType</p></th>
<th><p>Поддерживает метод должен возвращать значение True для всех этих констант</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>none</p></td>
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
> Несмотря на то, что **поддерживает**(**adUpdateBatch**) может иметь значение true для динамического и однонаправленные курсоры, для пакетного обновления следует использовать статический курсор или набора ключей. Присвойте свойству [LockType для](locktype-property-ado.md) **adLockBatchOptimistic** и **CursorLocation** свойства **adUseClient** , чтобы включить службу курсора для OLE DB, который необходим для пакетного обновления.

Свойство **CursorType** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.

**Службы удаленных данных об использовании** При использовании в объект набора записей со стороны клиента, свойство **CursorType** можно задать только к **adOpenStatic**.

