---
title: ActionEnum (Ссылка на настольные базы данных)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280658"
---
# <a name="actionenum"></a><span data-ttu-id="30442-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="30442-102">ActionEnum</span></span>

<span data-ttu-id="30442-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30442-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30442-104">Указывает тип действия, выполняемого при [вызвании SetPermissions.](setpermissions-method-adox.md)</span><span class="sxs-lookup"><span data-stu-id="30442-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30442-105">Константа</span><span class="sxs-lookup"><span data-stu-id="30442-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="30442-106">Значение</span><span class="sxs-lookup"><span data-stu-id="30442-106">Value</span></span></p></th>
<th><p><span data-ttu-id="30442-107">Описание</span><span class="sxs-lookup"><span data-stu-id="30442-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30442-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="30442-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="30442-109">3</span><span class="sxs-lookup"><span data-stu-id="30442-109">3</span></span></p></td>
<td><p><span data-ttu-id="30442-110">Группе или пользователю будет отказано в указанных разрешениях.</span><span class="sxs-lookup"><span data-stu-id="30442-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30442-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="30442-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="30442-112">1</span><span class="sxs-lookup"><span data-stu-id="30442-112">1</span></span></p></td>
<td><p><span data-ttu-id="30442-113">У группы или пользователя будут по крайней мере запрашиваемые разрешения.</span><span class="sxs-lookup"><span data-stu-id="30442-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30442-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="30442-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="30442-115">4 </span><span class="sxs-lookup"><span data-stu-id="30442-115">4</span></span></p></td>
<td><p><span data-ttu-id="30442-116">Любые явные права доступа, которые имеются у группы или пользователя, будут отменены.</span><span class="sxs-lookup"><span data-stu-id="30442-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30442-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="30442-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="30442-118">2</span><span class="sxs-lookup"><span data-stu-id="30442-118">2</span></span></p></td>
<td><p><span data-ttu-id="30442-119">У группы или пользователя будут именно запрашиваемые разрешения.</span><span class="sxs-lookup"><span data-stu-id="30442-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

