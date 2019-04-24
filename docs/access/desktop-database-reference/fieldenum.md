---
title: Фиелденум (Справочник по базам данных Access на компьютере)
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
# <a name="fieldenum"></a><span data-ttu-id="b6163-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="b6163-102">FieldEnum</span></span>

<span data-ttu-id="b6163-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6163-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6163-104">Указывает специальные поля, указанные в коллекции Fields объекта [](fields-collection-ado.md) [Record](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b6163-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6163-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b6163-105">Remarks</span></span>

<span data-ttu-id="b6163-106">Эти константы предоставляют "ярлык" для доступа к специальным полям, связанным с **записью**.</span><span class="sxs-lookup"><span data-stu-id="b6163-106">These constants provide a "shortcut" to accessing special fields associated with a **Record**.</span></span> <span data-ttu-id="b6163-107">ИзВлеките объект [field](field-object-ado.md) из коллекции **Fields** и получите его содержимое со свойством [value](value-property-ado.md) объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="b6163-107">Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6163-108">Константа</span><span class="sxs-lookup"><span data-stu-id="b6163-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="b6163-109">Значение</span><span class="sxs-lookup"><span data-stu-id="b6163-109">Value</span></span></p></th>
<th><p><span data-ttu-id="b6163-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b6163-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6163-111"><strong>Аддефаултстреам</strong></span><span class="sxs-lookup"><span data-stu-id="b6163-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="b6163-112">–1</span><span class="sxs-lookup"><span data-stu-id="b6163-112">-1</span></span></p></td>
<td><p><span data-ttu-id="b6163-113">Ссылается на поле, содержащее объект <a href="stream-object-ado.md">потока</a> по умолчанию, <strong></strong>связанный с записью.</span><span class="sxs-lookup"><span data-stu-id="b6163-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6163-114"><strong>Адрекордурл</strong></span><span class="sxs-lookup"><span data-stu-id="b6163-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="b6163-115">–2</span><span class="sxs-lookup"><span data-stu-id="b6163-115">-2</span></span></p></td>
<td><p><span data-ttu-id="b6163-116">Ссылается на поле, содержащее строку абсолютного URL-адреса для текущей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6163-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

