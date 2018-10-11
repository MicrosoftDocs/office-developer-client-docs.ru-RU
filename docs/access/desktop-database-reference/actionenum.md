---
title: ActionEnum (Справочник по для настольных баз данных Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af0e5fd734c03b88990383b99815d6e35f2c1290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480210"
---
# <a name="actionenum"></a><span data-ttu-id="b457b-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="b457b-102">ActionEnum</span></span>


<span data-ttu-id="b457b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b457b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b457b-104">Указывает тип действие, которое необходимо выполнить при вызове [SetPermissions](setpermissions-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="b457b-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b457b-105">Константа</span><span class="sxs-lookup"><span data-stu-id="b457b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b457b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b457b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b457b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b457b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b457b-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="b457b-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="b457b-109">3</span><span class="sxs-lookup"><span data-stu-id="b457b-109">3</span></span></p></td>
<td><p><span data-ttu-id="b457b-110">Группы или пользователи будет запрещен указанными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="b457b-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b457b-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="b457b-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="b457b-112">1</span><span class="sxs-lookup"><span data-stu-id="b457b-112">1</span></span></p></td>
<td><p><span data-ttu-id="b457b-113">Группы или пользователи будут иметь по крайней мере запрошенные разрешения.</span><span class="sxs-lookup"><span data-stu-id="b457b-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b457b-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="b457b-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="b457b-115">4</span><span class="sxs-lookup"><span data-stu-id="b457b-115">4</span></span></p></td>
<td><p><span data-ttu-id="b457b-116">Отменяется любое явный доступ права пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="b457b-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b457b-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="b457b-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="b457b-118">2</span><span class="sxs-lookup"><span data-stu-id="b457b-118">2</span></span></p></td>
<td><p><span data-ttu-id="b457b-119">Группы или пользователи будут иметь точно запрошенные разрешения.</span><span class="sxs-lookup"><span data-stu-id="b457b-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

