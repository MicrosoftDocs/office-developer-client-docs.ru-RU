---
title: Коллекция пользователей (ADOX)
TOCTitle: Users Collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3415fb7a2972621978ba3673343eb5f32b0eec1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885621"
---
# <a name="users-collection-adox"></a><span data-ttu-id="1f9cd-102">Коллекция пользователей (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1f9cd-102">Users Collection (ADOX)</span></span>


<span data-ttu-id="1f9cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f9cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f9cd-104">Содержит все хранимые объектов [пользователей](user-object-adox.md) из каталога или группы.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9cd-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f9cd-105">Remarks</span></span>

<span data-ttu-id="1f9cd-106">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-106">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="1f9cd-107">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="1f9cd-108">Метод [Append](append-method-adox-users.md) для семейства сайтов **пользователей** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-108">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX.</span></span> <span data-ttu-id="1f9cd-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-109">You can:</span></span>

  - <span data-ttu-id="1f9cd-110">Добавление нового пользователя в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="1f9cd-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="1f9cd-111">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="1f9cd-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-112">You can:</span></span>

  - <span data-ttu-id="1f9cd-113">Права пользователя в коллекции с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9cd-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="1f9cd-114">Возвращает количество пользователей, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9cd-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="1f9cd-115">Удаление пользователя из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9cd-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="1f9cd-116">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1f9cd-117">Перед добавлением объекта <STRONG>пользователя</STRONG> в коллекцию <STRONG>пользователей</STRONG> объекта <STRONG>группы</STRONG> , объект <STRONG>пользователя</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекции <STRONG>пользователей</STRONG> из <STRONG>каталога</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1f9cd-117">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


