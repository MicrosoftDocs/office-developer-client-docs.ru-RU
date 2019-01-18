---
title: Объект Group (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e010ac58ff0b573d42c562ce3be7a99acab5abea
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718170"
---
# <a name="group-object-adox"></a><span data-ttu-id="e66f4-102">Объект Group (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e66f4-102">Group object (ADOX)</span></span>


<span data-ttu-id="e66f4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e66f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e66f4-104">Представляет учетную запись группы, имеющей разрешения на доступ в рамках защищенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="e66f4-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="e66f4-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="e66f4-105">Remarks</span></span>

<span data-ttu-id="e66f4-106">Коллекция [групп](groups-collection-adox.md) [каталога](catalog-object-adox.md) представляет учетные записи групп каталога.</span><span class="sxs-lookup"><span data-stu-id="e66f4-106">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts.</span></span> <span data-ttu-id="e66f4-107">Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="e66f4-107">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="e66f4-108">С помощью свойства, семейств сайтов и методы объекта **группы** можно:</span><span class="sxs-lookup"><span data-stu-id="e66f4-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="e66f4-109">Идентификация группы с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e66f4-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="e66f4-110">Определите, будет ли группы имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e66f4-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="e66f4-111">Доступ к учетные записи пользователей, для которых членство в группе с помощью коллекции [пользователей](users-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e66f4-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="e66f4-112">Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e66f4-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

