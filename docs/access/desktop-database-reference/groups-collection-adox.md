---
title: Коллекция Groups (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21f1880a9effca6e51bc1e8b52a58dce22ce1ea9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292078"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="1fdfb-102">Коллекция Groups (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1fdfb-102">Groups collection (ADOX)</span></span>

<span data-ttu-id="1fdfb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fdfb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1fdfb-104">Содержит все объекты [группы](group-object-adox.md) , хранящиеся в каталоге или пользователе.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fdfb-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="1fdfb-105">Remarks</span></span>

<span data-ttu-id="1fdfb-106">Коллекция **Groups** [каталога](catalog-object-adox.md) представляет все учетные записи групп в каталоге.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-106">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="1fdfb-107">Коллекция **Groups** для [пользователя](user-object-adox.md) представляет только группу, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-107">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="1fdfb-108">Метод [append](append-method-adox-groups.md) коллекции **GROUPS** уникален для ADOX.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-108">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX.</span></span> <span data-ttu-id="1fdfb-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-109">You can:</span></span>

- <span data-ttu-id="1fdfb-110">Добавьте новую группу безопасности в коллекцию с помощью метода **append** .</span><span class="sxs-lookup"><span data-stu-id="1fdfb-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="1fdfb-111">Остальные свойства и методы являются стандартными для коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="1fdfb-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-112">You can:</span></span>

- <span data-ttu-id="1fdfb-113">Доступ к группе в коллекции со свойством [Item](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1fdfb-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="1fdfb-114">Возвращает количество групп, содержащиеся в коллекции, со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1fdfb-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="1fdfb-115">Удаление группы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="1fdfb-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="1fdfb-116">Обновление объектов в коллекции в соответствии с схемой текущей базы данных с помощью метода [Refresh](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1fdfb-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="1fdfb-117">Перед добавлением объекта **Group** в коллекцию **Groups** объекта **User** объект **Group** с тем же [именем](name-property-adox.md) , что и у добавляемого объекта, должен уже существовать в коллекции **Groups** **каталога**.</span><span class="sxs-lookup"><span data-stu-id="1fdfb-117">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


