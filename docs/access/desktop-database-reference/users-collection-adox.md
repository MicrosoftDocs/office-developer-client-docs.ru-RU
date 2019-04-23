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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312938"
---
# <a name="users-collection-adox"></a><span data-ttu-id="21a13-102">Коллекция Users (ADOX)</span><span class="sxs-lookup"><span data-stu-id="21a13-102">Users collection (ADOX)</span></span>

<span data-ttu-id="21a13-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21a13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21a13-104">Содержит все сохраненные объекты [пользователя](user-object-adox.md) для каталога или группы.</span><span class="sxs-lookup"><span data-stu-id="21a13-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="21a13-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="21a13-105">Remarks</span></span>

<span data-ttu-id="21a13-106">Коллекция **Users** [каталога](catalog-object-adox.md) Users содержит все пользователи каталога.</span><span class="sxs-lookup"><span data-stu-id="21a13-106">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="21a13-107">Коллекция **Users** для [группы](group-object-adox.md) представляет только тех пользователей, у которых есть членство в определенной группе.</span><span class="sxs-lookup"><span data-stu-id="21a13-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="21a13-108">Метод [append](append-method-adox-users.md) для коллекции **Users** уникален для ADOX.</span><span class="sxs-lookup"><span data-stu-id="21a13-108">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX.</span></span> <span data-ttu-id="21a13-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="21a13-109">You can:</span></span>

- <span data-ttu-id="21a13-110">Добавьте нового пользователя в коллекцию с помощью метода **append** .</span><span class="sxs-lookup"><span data-stu-id="21a13-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="21a13-111">Остальные свойства и методы являются стандартными для коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="21a13-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="21a13-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="21a13-112">You can:</span></span>

- <span data-ttu-id="21a13-113">Доступ к пользователю в коллекции со свойством [Item](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="21a13-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="21a13-114">Возврат числа пользователей, включенных в коллекцию, со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="21a13-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="21a13-115">Удаление пользователя из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="21a13-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="21a13-116">Обновление объектов в коллекции в соответствии с схемой текущей базы данных с помощью метода [Refresh](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="21a13-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="21a13-117">Перед добавлением объекта **User** в коллекцию **Users** объекта **Group** объект **пользователя** с тем же [именем](name-property-adox.md) , что и у добавляемОго объекта, должен уже существовать в коллекции Users **каталога**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="21a13-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

