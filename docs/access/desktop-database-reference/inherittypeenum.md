---
title: InheritTypeEnum (Ссылка на настольные базы данных)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291416"
---
# <a name="inherittypeenum"></a><span data-ttu-id="8a0fa-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="8a0fa-102">InheritTypeEnum</span></span>

<span data-ttu-id="8a0fa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a0fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a0fa-104">Указывает, как объекты будут наследовать разрешения, заданные [с помощью SetPermissions.](setpermissions-method-adox.md)</span><span class="sxs-lookup"><span data-stu-id="8a0fa-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a0fa-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8a0fa-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8a0fa-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8a0fa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8a0fa-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8a0fa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a0fa-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="8a0fa-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="8a0fa-109">3</span><span class="sxs-lookup"><span data-stu-id="8a0fa-109">3</span></span></p></td>
<td><p><span data-ttu-id="8a0fa-110">И объекты, и другие контейнеры, содержащиеся в основном объекте, наследуют запись.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a0fa-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="8a0fa-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="8a0fa-112">2</span><span class="sxs-lookup"><span data-stu-id="8a0fa-112">2</span></span></p></td>
<td><p><span data-ttu-id="8a0fa-113">Другие контейнеры, содержащиеся в основном объекте, наследуют запись.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a0fa-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="8a0fa-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="8a0fa-115">0</span><span class="sxs-lookup"><span data-stu-id="8a0fa-115">0</span></span></p></td>
<td><p><span data-ttu-id="8a0fa-116">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-116">Default.</span></span> <span data-ttu-id="8a0fa-117">Наследование не происходит.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-117">No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a0fa-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="8a0fa-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="8a0fa-119">4 </span><span class="sxs-lookup"><span data-stu-id="8a0fa-119">4</span></span></p></td>
<td><p><span data-ttu-id="8a0fa-120">Флаги <strong>adInheritObjects</strong> и <strong>adInheritContainers</strong> не распространяются на наследуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a0fa-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="8a0fa-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="8a0fa-122">1</span><span class="sxs-lookup"><span data-stu-id="8a0fa-122">1</span></span></p></td>
<td><p><span data-ttu-id="8a0fa-123">Не контейнерные объекты в контейнере наследуют разрешения.</span><span class="sxs-lookup"><span data-stu-id="8a0fa-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

