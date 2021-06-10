---
title: Объект group (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e010ac58ff0b573d42c562ce3be7a99acab5abea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292120"
---
# <a name="group-object-adox"></a><span data-ttu-id="b3b7f-102">Объект group (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b3b7f-102">Group object (ADOX)</span></span>


<span data-ttu-id="b3b7f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3b7f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3b7f-104">Представляет учетную запись группы, которая имеет разрешения на доступ в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="b3b7f-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b7f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3b7f-105">Remarks</span></span>

<span data-ttu-id="b3b7f-106">Коллекция [Групп](groups-collection-adox.md) [каталога](catalog-object-adox.md) представляет все учетные записи группы каталога.</span><span class="sxs-lookup"><span data-stu-id="b3b7f-106">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts.</span></span> <span data-ttu-id="b3b7f-107">Коллекция **Groups** для [пользователя представляет](user-object-adox.md) только группу, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="b3b7f-107">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="b3b7f-108">С помощью свойств, коллекций и методов объекта **Group** можно:</span><span class="sxs-lookup"><span data-stu-id="b3b7f-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="b3b7f-109">Определите группу с [свойством Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="b3b7f-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="b3b7f-110">Определите, читала ли группа разрешения, писала или удаляла их с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions.](setpermissions-method-adox.md)</span><span class="sxs-lookup"><span data-stu-id="b3b7f-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="b3b7f-111">Доступ к учетным записям пользователей, которые имеют членство в группе с [коллекцией Пользователей.](users-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="b3b7f-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="b3b7f-112">Доступ к свойствам, определенным поставщикам, с [коллекцией свойств.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3b7f-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

