---
title: Коллекция групп (ADOX)
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
# <a name="groups-collection-adox"></a><span data-ttu-id="e58d0-102">Коллекция групп (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e58d0-102">Groups collection (ADOX)</span></span>

<span data-ttu-id="e58d0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e58d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e58d0-104">Содержит все сохраненные [объекты Group](group-object-adox.md) каталога или пользователя.</span><span class="sxs-lookup"><span data-stu-id="e58d0-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="e58d0-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e58d0-105">Remarks</span></span>

<span data-ttu-id="e58d0-106">Коллекция **Групп** [каталога](catalog-object-adox.md) представляет все учетные записи группы каталога.</span><span class="sxs-lookup"><span data-stu-id="e58d0-106">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="e58d0-107">Коллекция **Groups** для [пользователя представляет](user-object-adox.md) только группу, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="e58d0-107">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="e58d0-108">Метод [Приложения](append-method-adox-groups.md) для коллекции **Groups** уникален для ADOX.</span><span class="sxs-lookup"><span data-stu-id="e58d0-108">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX.</span></span> <span data-ttu-id="e58d0-109">Вы получаете перечисленные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="e58d0-109">You can:</span></span>

- <span data-ttu-id="e58d0-110">Добавьте новую группу безопасности в коллекцию с помощью метода **Приложения.**</span><span class="sxs-lookup"><span data-stu-id="e58d0-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="e58d0-111">Остальные свойства и методы являются стандартными для коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="e58d0-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="e58d0-112">Вы получаете перечисленные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="e58d0-112">You can:</span></span>

- <span data-ttu-id="e58d0-113">Доступ к группе в коллекции с [свойством Item.](item-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="e58d0-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="e58d0-114">Возвращайте количество групп, содержащихся в коллекции, с [свойством Count.](count-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="e58d0-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="e58d0-115">Удалите группу из коллекции методом [Delete.](delete-method-adox-collections.md)</span><span class="sxs-lookup"><span data-stu-id="e58d0-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="e58d0-116">Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью [метода Обновления.](refresh-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="e58d0-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="e58d0-117">Прежде чем примковать  объект **Group**  к коллекции Групп объекта Пользователя, объект **Group** с тем же именем, что и объект, который должен быть придан, уже должен существовать в коллекции **Groups** **каталога.** [](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="e58d0-117">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


