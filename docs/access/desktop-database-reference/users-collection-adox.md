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
# <a name="users-collection-adox"></a><span data-ttu-id="766cd-102">Коллекция Users (ADOX)</span><span class="sxs-lookup"><span data-stu-id="766cd-102">Users collection (ADOX)</span></span>

<span data-ttu-id="766cd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="766cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="766cd-104">Содержит все [хранимые](user-object-adox.md) объекты пользователя каталога или группы.</span><span class="sxs-lookup"><span data-stu-id="766cd-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="766cd-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="766cd-105">Remarks</span></span>

<span data-ttu-id="766cd-106">Коллекция **"Пользователи"** [каталога](catalog-object-adox.md) представляет всех пользователей каталога.</span><span class="sxs-lookup"><span data-stu-id="766cd-106">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="766cd-107">Коллекция **Users** для [группы представляет](group-object-adox.md) только пользователей, которые являются членами определенной группы.</span><span class="sxs-lookup"><span data-stu-id="766cd-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="766cd-108">Метод [Append](append-method-adox-users.md) для коллекции **Users** уникален для ADOX.</span><span class="sxs-lookup"><span data-stu-id="766cd-108">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX.</span></span> <span data-ttu-id="766cd-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="766cd-109">You can:</span></span>

- <span data-ttu-id="766cd-110">Добавьте нового пользователя в коллекцию с помощью метода **Append.**</span><span class="sxs-lookup"><span data-stu-id="766cd-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="766cd-111">Остальные свойства и методы являются стандартными для коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="766cd-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="766cd-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="766cd-112">You can:</span></span>

- <span data-ttu-id="766cd-113">Доступ к пользователю в коллекции с помощью [свойства Item.](item-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="766cd-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="766cd-114">Возвращает количество пользователей, содержащихся в коллекции, со свойством [Count.](count-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="766cd-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="766cd-115">Удаление пользователя из коллекции с помощью метода [Delete.](delete-method-adox-collections.md)</span><span class="sxs-lookup"><span data-stu-id="766cd-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="766cd-116">Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью метода [Refresh.](refresh-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="766cd-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="766cd-117">Прежде чем приместь объект [](name-property-adox.md) **User** к коллекции **Users** объекта **Group,** объект **User** с тем же именем, что и объект, который необходимо к ним примедить, должен уже существовать в коллекции **Users** **каталога.**</span><span class="sxs-lookup"><span data-stu-id="766cd-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

