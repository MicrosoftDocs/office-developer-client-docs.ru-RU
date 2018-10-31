---
title: FieldEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9ab46fc7c3817cbfa83c78816a42472e425d2d71
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860051"
---
# <a name="fieldenum"></a><span data-ttu-id="7509f-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="7509f-102">FieldEnum</span></span>

<span data-ttu-id="7509f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7509f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7509f-104">Задает особых полей, указанных в коллекции [полей](fields-collection-ado.md) объект [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7509f-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7509f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="7509f-105">Remarks</span></span>

<span data-ttu-id="7509f-106">Эти константы предоставляют «ярлык» для доступа к особых полей, сопоставленных с **записи**.</span><span class="sxs-lookup"><span data-stu-id="7509f-106">These constants provide a "shortcut" to accessing special fields associated with a **Record**.</span></span> <span data-ttu-id="7509f-107">Получение объекта [поля](field-object-ado.md) из коллекции **полей** и получение его содержимое с помощью свойства [Value](value-property-ado.md) объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="7509f-107">Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7509f-108">Константа</span><span class="sxs-lookup"><span data-stu-id="7509f-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="7509f-109">Значение</span><span class="sxs-lookup"><span data-stu-id="7509f-109">Value</span></span></p></th>
<th><p><span data-ttu-id="7509f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7509f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7509f-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="7509f-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="7509f-112">-1</span><span class="sxs-lookup"><span data-stu-id="7509f-112">-1</span></span></p></td>
<td><p><span data-ttu-id="7509f-113">Ссылается на поле, содержащее объект <a href="stream-object-ado.md">потока</a> по умолчанию, связанный с <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="7509f-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7509f-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="7509f-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="7509f-115">-2</span><span class="sxs-lookup"><span data-stu-id="7509f-115">-2</span></span></p></td>
<td><p><span data-ttu-id="7509f-116">Ссылается на поле, содержащее строку абсолютный URL-адрес для текущей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="7509f-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

