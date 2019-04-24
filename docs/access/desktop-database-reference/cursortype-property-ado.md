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

Указывает тип курсора, используемого в объекте [Recordset](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [курсортипинум](cursortypeenum.md) . Значение по умолчанию — **адопенфорвардонли**.

## <a name="remarks"></a>Замечания

Используйте свойство **CursorType** , чтобы указать тип курсора, который следует использовать при открытии объекта **Recordset** .

Если свойству [CursorLocation](cursorlocation-property-ado.md) присвоено значение **Адусеклиент**, поддерживается только параметр **адопенстатик** . Если задано неподдерживаемое значение, ошибка не будет возникать; Вместо этого будет использоваться ближайшее поддерживаемое **CursorType** .

Если поставщик не поддерживает запрошенный тип курсора, он может вернуть другой тип курсора. Свойство **CursorType** будет изменено для согласования с фактическим типом курсора, используемым при открытии объекта [Recordset](recordset-object-ado.md) . Чтобы проверить определенные функциональные возможности возвращаемого курсора, используйте [](supports-method-ado.md) метод Supports. После закрытия **набора записей**свойство **CursorType** возвращается к исходному значению.

На следующей диаграмме показаны функциональные возможности поставщика (определяемые с помощью констант методов), необходимые для каждого типа курсора. ****

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Для набора записей этого CursorType</p></th>
<th><p>Метод Supports должен возвращать значение true для всех этих констант</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Адопенфорвардонли</strong></p></td>
<td><p>нет</p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенкэйсет</strong></p></td>
<td><p><strong>адбукмарк</strong>, <strong>адхолдрекордс</strong>, <strong>адмовепревиаус</strong>, <strong>адресинк</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Адопендинамик</strong></p></td>
<td><p><strong>Адмовепревиаус</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенстатик</strong></p></td>
<td><p><strong>адбукмарк</strong>, <strong>адхолдрекордс</strong>, <strong>адмовепревиаус</strong>, <strong>адресинк</strong></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Несмотря на то, что **поддерживается**(**адупдатебатч**) для динамических однонаправленных курсоров и однонаправленных курсоров, для пакетных обновлений необходимо использовать указатель KEYSET или статический. ПриСвойте свойству [LockType](locktype-property-ado.md) значение **адлоккбатчоптимистик** , а свойству **CursorLocation** — значение **адусеклиент** , чтобы включить службу курсора для OLE DB, которая необходима для пакетных обновлений.

Свойство **CursorType** доступно для чтения и записи, когда **набор записей** закрывается и только для чтения, когда он открыт.

**Использование удаленной службы данных** При использовании в объекте Recordset на стороне клиента свойство **CursorType** можно задать только для **адопенстатик**.

