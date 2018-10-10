---
title: FieldEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5efcdbd9da4214d7f2b78ffbcfb81fb13265087e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479944"
---
# <a name="fieldenum"></a><span data-ttu-id="98741-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="98741-102">FieldEnum</span></span>


<span data-ttu-id="98741-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98741-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98741-104">Задает особых полей, указанных в коллекции [полей](fields-collection-ado.md) объект [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="98741-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

<span data-ttu-id="98741-105">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="98741-105">**Remarks**</span></span>

<span data-ttu-id="98741-106">Эти константы предоставляют «ярлык» для доступа к особых полей, сопоставленных с **записи**.</span><span class="sxs-lookup"><span data-stu-id="98741-106">These constants provide a "shortcut" to accessing special fields associated with a **Record**.</span></span> <span data-ttu-id="98741-107">Получение объекта [поля](field-object-ado.md) из коллекции **полей** и получение его содержимое с помощью свойства [Value](value-property-ado.md) объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="98741-107">Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98741-108">Константа</span><span class="sxs-lookup"><span data-stu-id="98741-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="98741-109">Значение</span><span class="sxs-lookup"><span data-stu-id="98741-109">Value</span></span></p></th>
<th><p><span data-ttu-id="98741-110">Описание</span><span class="sxs-lookup"><span data-stu-id="98741-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98741-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="98741-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="98741-112">-1</span><span class="sxs-lookup"><span data-stu-id="98741-112">-1</span></span></p></td>
<td><p><span data-ttu-id="98741-113">Ссылается на поле, содержащее объект <a href="stream-object-ado.md">потока</a> по умолчанию, связанный с <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="98741-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98741-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="98741-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="98741-115">-2</span><span class="sxs-lookup"><span data-stu-id="98741-115">-2</span></span></p></td>
<td><p><span data-ttu-id="98741-116">Ссылается на поле, содержащее строку абсолютный URL-адрес для текущей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="98741-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

