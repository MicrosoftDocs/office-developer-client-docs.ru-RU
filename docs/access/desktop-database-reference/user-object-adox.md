---
title: Объект пользователя (ADOX — ссылка на базу данных для настольных компьютеров)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313162"
---
# <a name="user-object-adox"></a><span data-ttu-id="87a34-102">Объект пользователя (ADOX)</span><span class="sxs-lookup"><span data-stu-id="87a34-102">User object (ADOX)</span></span>


<span data-ttu-id="87a34-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87a34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87a34-104">Представляет учетную запись пользователя с разрешениями доступа в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="87a34-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="87a34-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="87a34-105">Remarks</span></span>

<span data-ttu-id="87a34-106">Коллекция ["Пользователи](users-collection-adox.md) [каталога"](catalog-object-adox.md) представляет всех пользователей каталога.</span><span class="sxs-lookup"><span data-stu-id="87a34-106">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="87a34-107">Коллекция **Пользователей** для [группы](group-object-adox.md) представляет только пользователей определенной группы.</span><span class="sxs-lookup"><span data-stu-id="87a34-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="87a34-108">С помощью свойств, коллекций и методов объекта **Пользователя** можно:</span><span class="sxs-lookup"><span data-stu-id="87a34-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="87a34-109">Определите пользователя с [свойством Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="87a34-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="87a34-110">Измените пароль для пользователя методом [ChangePassword.](changepassword-method-adox.md)</span><span class="sxs-lookup"><span data-stu-id="87a34-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="87a34-111">Определите, читал ли пользователь, писал или удалял разрешения с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions.](setpermissions-method-adox.md)</span><span class="sxs-lookup"><span data-stu-id="87a34-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="87a34-112">Доступ к группам, к которым принадлежит пользователь в коллекции [Groups.](groups-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="87a34-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="87a34-113">Доступ к свойствам, определенным поставщикам, с [коллекцией свойств.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="87a34-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

