---
title: Объект группы (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f98e65522ebefdb8f3897234d04e54d9599dda
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883682"
---
# <a name="group-object-adox"></a><span data-ttu-id="60161-102">Объект группы (ADOX)</span><span class="sxs-lookup"><span data-stu-id="60161-102">Group Object (ADOX)</span></span>


<span data-ttu-id="60161-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60161-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60161-104">Представляет учетную запись группы, имеющей разрешения на доступ в рамках защищенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="60161-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="60161-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="60161-105">Remarks</span></span>

<span data-ttu-id="60161-106">Коллекция [групп](groups-collection-adox.md) [каталога](catalog-object-adox.md) представляет учетные записи групп каталога.</span><span class="sxs-lookup"><span data-stu-id="60161-106">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts.</span></span> <span data-ttu-id="60161-107">Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="60161-107">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="60161-108">С помощью свойства, семейств сайтов и методы объекта **группы** можно:</span><span class="sxs-lookup"><span data-stu-id="60161-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="60161-109">Идентификация группы с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="60161-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="60161-110">Определите, будет ли группы имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="60161-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="60161-111">Доступ к учетные записи пользователей, для которых членство в группе с помощью коллекции [пользователей](users-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="60161-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="60161-112">Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="60161-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

