---
title: InheritTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: df631319abc1eba06d7ac804b6d8dbdaf5fc9b18
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888053"
---
# <a name="inherittypeenum"></a><span data-ttu-id="e6e67-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="e6e67-102">InheritTypeEnum</span></span>

<span data-ttu-id="e6e67-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6e67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6e67-104">Указывает, как будет наследуют разрешения, установленные с [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e6e67-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6e67-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e6e67-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e6e67-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e6e67-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e6e67-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e6e67-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6e67-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="e6e67-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e67-109">3</span><span class="sxs-lookup"><span data-stu-id="e6e67-109">3</span></span></p></td>
<td><p><span data-ttu-id="e6e67-110">Объекты и другие контейнеры, содержащихся в основных объекте наследовать словом.</span><span class="sxs-lookup"><span data-stu-id="e6e67-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e67-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="e6e67-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e67-112">2</span><span class="sxs-lookup"><span data-stu-id="e6e67-112">2</span></span></p></td>
<td><p><span data-ttu-id="e6e67-113">Другие контейнеры, содержащиеся в объекте основной наследовать словом.</span><span class="sxs-lookup"><span data-stu-id="e6e67-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e67-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="e6e67-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e67-115">0</span><span class="sxs-lookup"><span data-stu-id="e6e67-115">0</span></span></p></td>
<td><p><span data-ttu-id="e6e67-116">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6e67-116">Default.</span></span> <span data-ttu-id="e6e67-117">Наследование не происходит.</span><span class="sxs-lookup"><span data-stu-id="e6e67-117">No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e67-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="e6e67-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e67-119">4</span><span class="sxs-lookup"><span data-stu-id="e6e67-119">4</span></span></p></td>
<td><p><span data-ttu-id="e6e67-120">Флаги <strong>adInheritObjects</strong> и <strong>adInheritContainers</strong> не распространяются на наследуемые записи.</span><span class="sxs-lookup"><span data-stu-id="e6e67-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e67-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="e6e67-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e67-122">1</span><span class="sxs-lookup"><span data-stu-id="e6e67-122">1</span></span></p></td>
<td><p><span data-ttu-id="e6e67-123">Non контейнер объектов в контейнере наследовать разрешения.</span><span class="sxs-lookup"><span data-stu-id="e6e67-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

