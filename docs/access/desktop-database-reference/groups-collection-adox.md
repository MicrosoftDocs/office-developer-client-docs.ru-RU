---
title: Коллекция Groups (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7bd2519af3ea3c35d8cc32ef1ec31ea4f9efa1e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936674"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="2b58f-102">Коллекция Groups (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2b58f-102">Groups collection (ADOX)</span></span>

<span data-ttu-id="2b58f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b58f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b58f-104">Содержит все хранимые объекты [групповой](group-object-adox.md) каталога или пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b58f-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b58f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b58f-105">Remarks</span></span>

<span data-ttu-id="2b58f-106">Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога.</span><span class="sxs-lookup"><span data-stu-id="2b58f-106">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="2b58f-107">Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="2b58f-107">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="2b58f-108">Метод [Append](append-method-adox-groups.md) для семейства сайтов **групп** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="2b58f-108">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX.</span></span> <span data-ttu-id="2b58f-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2b58f-109">You can:</span></span>

- <span data-ttu-id="2b58f-110">Добавление новой группы безопасности в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="2b58f-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="2b58f-111">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="2b58f-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="2b58f-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2b58f-112">You can:</span></span>

- <span data-ttu-id="2b58f-113">Доступ к группы в семействе сайтов с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2b58f-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="2b58f-114">Возвращает число групп, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2b58f-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="2b58f-115">Удаление группы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="2b58f-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="2b58f-116">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="2b58f-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="2b58f-117">Перед добавлением объекта **группы** в коллекцию **групп** объекта **пользователя** , объект **группы** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекцию **групп** **каталога**.</span><span class="sxs-lookup"><span data-stu-id="2b58f-117">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


