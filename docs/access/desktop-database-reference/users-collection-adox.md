---
title: Коллекция Users (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3d91af56dc37cf8719a241a35046d663f7c9d57
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998075"
---
# <a name="users-collection-adox"></a><span data-ttu-id="05b49-102">Коллекция Users (ADOX)</span><span class="sxs-lookup"><span data-stu-id="05b49-102">Users collection (ADOX)</span></span>

<span data-ttu-id="05b49-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05b49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05b49-104">Содержит все хранимые объектов [пользователей](user-object-adox.md) из каталога или группы.</span><span class="sxs-lookup"><span data-stu-id="05b49-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b49-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="05b49-105">Remarks</span></span>

<span data-ttu-id="05b49-106">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="05b49-106">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="05b49-107">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="05b49-107">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="05b49-108">Метод [Append](append-method-adox-users.md) для семейства сайтов **пользователей** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="05b49-108">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX.</span></span> <span data-ttu-id="05b49-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="05b49-109">You can:</span></span>

- <span data-ttu-id="05b49-110">Добавление нового пользователя в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="05b49-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="05b49-111">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="05b49-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="05b49-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="05b49-112">You can:</span></span>

- <span data-ttu-id="05b49-113">Права пользователя в коллекции с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="05b49-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="05b49-114">Возвращает количество пользователей, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="05b49-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="05b49-115">Удаление пользователя из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="05b49-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="05b49-116">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="05b49-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="05b49-117">Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.</span><span class="sxs-lookup"><span data-stu-id="05b49-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

