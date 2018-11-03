---
title: Коллекция Users (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b44b7b858adca5672266eb1898213d8f28429f2e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931136"
---
# <a name="users-collection-adox"></a><span data-ttu-id="3756c-102">Коллекция Users (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3756c-102">Users collection (ADOX)</span></span>


<span data-ttu-id="3756c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3756c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3756c-104">Содержит все хранимые объектов [пользователей](user-object-adox.md) из каталога или группы.</span><span class="sxs-lookup"><span data-stu-id="3756c-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="3756c-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="3756c-105">Remarks</span></span>

<span data-ttu-id="3756c-106">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="3756c-106">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="3756c-107">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="3756c-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="3756c-108">Метод [Append](append-method-adox-users.md) для семейства сайтов **пользователей** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="3756c-108">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX.</span></span> <span data-ttu-id="3756c-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3756c-109">You can:</span></span>

  - <span data-ttu-id="3756c-110">Добавление нового пользователя в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="3756c-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="3756c-111">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="3756c-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="3756c-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3756c-112">You can:</span></span>

  - <span data-ttu-id="3756c-113">Права пользователя в коллекции с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3756c-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="3756c-114">Возвращает количество пользователей, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3756c-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="3756c-115">Удаление пользователя из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="3756c-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="3756c-116">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="3756c-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3756c-117">Перед добавлением объекта <STRONG>пользователя</STRONG> в коллекцию <STRONG>пользователей</STRONG> объекта <STRONG>группы</STRONG> , объект <STRONG>пользователя</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекции <STRONG>пользователей</STRONG> из <STRONG>каталога</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3756c-117">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


