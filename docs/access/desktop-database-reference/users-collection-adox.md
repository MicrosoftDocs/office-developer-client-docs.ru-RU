---
title: Коллекция Users (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720410"
---
# <a name="users-collection-adox"></a><span data-ttu-id="26448-102">Коллекция Users (ADOX)</span><span class="sxs-lookup"><span data-stu-id="26448-102">Users collection (ADOX)</span></span>

<span data-ttu-id="26448-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26448-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26448-104">Содержит все хранимые объектов [пользователей](user-object-adox.md) из каталога или группы.</span><span class="sxs-lookup"><span data-stu-id="26448-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="26448-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="26448-105">Remarks</span></span>

<span data-ttu-id="26448-106">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="26448-106">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="26448-107">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="26448-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="26448-108">Метод [Append](append-method-adox-users.md) для семейства сайтов **пользователей** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="26448-108">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX.</span></span> <span data-ttu-id="26448-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="26448-109">You can:</span></span>

- <span data-ttu-id="26448-110">Добавление нового пользователя в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="26448-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="26448-111">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="26448-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="26448-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="26448-112">You can:</span></span>

- <span data-ttu-id="26448-113">Права пользователя в коллекции с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="26448-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="26448-114">Возвращает количество пользователей, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="26448-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="26448-115">Удаление пользователя из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="26448-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="26448-116">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="26448-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="26448-117">Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.</span><span class="sxs-lookup"><span data-stu-id="26448-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

