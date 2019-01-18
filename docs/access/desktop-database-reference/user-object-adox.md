---
title: Объект пользователя (ADOX - ссылки для настольных баз данных Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702616"
---
# <a name="user-object-adox"></a><span data-ttu-id="7a8ae-102">Объект User (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7a8ae-102">User object (ADOX)</span></span>


<span data-ttu-id="7a8ae-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a8ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a8ae-104">Представляет учетную запись пользователя, который имеет разрешения на доступ в рамках защищенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7a8ae-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a8ae-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a8ae-105">Remarks</span></span>

<span data-ttu-id="7a8ae-106">Коллекция [пользователей](users-collection-adox.md) из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="7a8ae-106">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="7a8ae-107">Коллекция **пользователей** для [группы](group-object-adox.md) представляет только пользователи конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="7a8ae-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="7a8ae-108">С помощью свойства, семейств сайтов и методы объекта **пользователя** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7a8ae-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="7a8ae-109">Определите пользователя с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8ae-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="7a8ae-110">Изменение пароля для пользователя с помощью метода [Изменение пароля](changepassword-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8ae-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="7a8ae-111">Определить, является ли пользователь имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8ae-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="7a8ae-112">Доступ к групп, к которым принадлежит пользователь с коллекцией [групп](groups-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8ae-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="7a8ae-113">Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8ae-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

