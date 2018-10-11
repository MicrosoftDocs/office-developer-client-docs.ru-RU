---
title: InheritTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 031c47aff666bf10f0e2aa597ccd0143ed3d6209
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480288"
---
# <a name="inherittypeenum"></a><span data-ttu-id="3ba54-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="3ba54-102">InheritTypeEnum</span></span>


<span data-ttu-id="3ba54-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ba54-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ba54-104">Указывает, как будет наследуют разрешения, установленные с [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="3ba54-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ba54-105">Константа</span><span class="sxs-lookup"><span data-stu-id="3ba54-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3ba54-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3ba54-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3ba54-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3ba54-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ba54-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="3ba54-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="3ba54-109">3</span><span class="sxs-lookup"><span data-stu-id="3ba54-109">3</span></span></p></td>
<td><p><span data-ttu-id="3ba54-110">Объекты и другие контейнеры, содержащихся в основных объекте наследовать словом.</span><span class="sxs-lookup"><span data-stu-id="3ba54-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ba54-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="3ba54-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="3ba54-112">2</span><span class="sxs-lookup"><span data-stu-id="3ba54-112">2</span></span></p></td>
<td><p><span data-ttu-id="3ba54-113">Другие контейнеры, содержащиеся в объекте основной наследовать словом.</span><span class="sxs-lookup"><span data-stu-id="3ba54-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ba54-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="3ba54-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="3ba54-115">0</span><span class="sxs-lookup"><span data-stu-id="3ba54-115">0</span></span></p></td>
<td><p><span data-ttu-id="3ba54-116">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ba54-116">Default.</span></span> <span data-ttu-id="3ba54-117">Наследование не происходит.</span><span class="sxs-lookup"><span data-stu-id="3ba54-117">No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ba54-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="3ba54-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="3ba54-119">4</span><span class="sxs-lookup"><span data-stu-id="3ba54-119">4</span></span></p></td>
<td><p><span data-ttu-id="3ba54-120">Флаги <strong>adInheritObjects</strong> и <strong>adInheritContainers</strong> не распространяются на наследуемые записи.</span><span class="sxs-lookup"><span data-stu-id="3ba54-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ba54-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="3ba54-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="3ba54-122">1</span><span class="sxs-lookup"><span data-stu-id="3ba54-122">1</span></span></p></td>
<td><p><span data-ttu-id="3ba54-123">Non контейнер объектов в контейнере наследовать разрешения.</span><span class="sxs-lookup"><span data-stu-id="3ba54-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

