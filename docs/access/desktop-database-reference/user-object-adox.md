---
title: Объект пользователя (ADOX - ссылки для настольных баз данных Access)
TOCTitle: User Object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab5d92a67737774d817046538200d0ebd4337e74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481809"
---
# <a name="user-object-adox"></a><span data-ttu-id="864f8-102">User Object (ADOX)</span><span class="sxs-lookup"><span data-stu-id="864f8-102">User Object (ADOX)</span></span>


<span data-ttu-id="864f8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="864f8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="864f8-104">Представляет учетную запись пользователя, который имеет разрешения на доступ в рамках защищенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="864f8-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="864f8-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="864f8-105">Remarks</span></span>

<span data-ttu-id="864f8-106">Коллекция [пользователей](users-collection-adox.md) из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="864f8-106">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="864f8-107">Коллекция **пользователей** для [группы](group-object-adox.md) представляет только пользователи конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="864f8-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="864f8-108">С помощью свойства, семейств сайтов и методы объекта **пользователя** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="864f8-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="864f8-109">Определите пользователя с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="864f8-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="864f8-110">Изменение пароля для пользователя с помощью метода [Изменение пароля](changepassword-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="864f8-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="864f8-111">Определить, является ли пользователь имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="864f8-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="864f8-112">Доступ к групп, к которым принадлежит пользователь с коллекцией [групп](groups-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="864f8-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="864f8-113">Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="864f8-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

