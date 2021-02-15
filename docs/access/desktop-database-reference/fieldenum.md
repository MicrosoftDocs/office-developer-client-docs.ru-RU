---
title: FieldEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292596"
---
# <a name="fieldenum"></a><span data-ttu-id="48175-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="48175-102">FieldEnum</span></span>

<span data-ttu-id="48175-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48175-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48175-104">Указывает специальные поля, на которые ссылается коллекция [Fields](record-object-ado.md) объекта [Record.](fields-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="48175-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="48175-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="48175-105">Remarks</span></span>

<span data-ttu-id="48175-106">Эти константы предоставляют "ярлык" для доступа к специальным полям, связанным с **записью.**</span><span class="sxs-lookup"><span data-stu-id="48175-106">These constants provide a "shortcut" to accessing special fields associated with a **Record**.</span></span> <span data-ttu-id="48175-107">Получите объект [Field](field-object-ado.md) из коллекции **Fields,** а затем получите его содержимое с помощью свойства **Value** объекта [Field.](value-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="48175-107">Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48175-108">Константа</span><span class="sxs-lookup"><span data-stu-id="48175-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="48175-109">Значение</span><span class="sxs-lookup"><span data-stu-id="48175-109">Value</span></span></p></th>
<th><p><span data-ttu-id="48175-110">Описание</span><span class="sxs-lookup"><span data-stu-id="48175-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48175-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="48175-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="48175-112">–1</span><span class="sxs-lookup"><span data-stu-id="48175-112">-1</span></span></p></td>
<td><p><span data-ttu-id="48175-113">Ссылается на поле, содержащее <a href="stream-object-ado.md">объект Stream по</a> умолчанию, связанный с <strong>записью.</strong></span><span class="sxs-lookup"><span data-stu-id="48175-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48175-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="48175-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="48175-115">–2</span><span class="sxs-lookup"><span data-stu-id="48175-115">-2</span></span></p></td>
<td><p><span data-ttu-id="48175-116">Ссылается на поле, содержащее строку абсолютного URL-адреса для текущей <strong>записи.</strong></span><span class="sxs-lookup"><span data-stu-id="48175-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

