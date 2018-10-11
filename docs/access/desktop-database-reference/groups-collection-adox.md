---
title: Groups Collection (ADOX)
TOCTitle: Groups Collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e7021d6dc485d4c0cfbeca4b9fe487817de715f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481770"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="b0365-102">Groups Collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b0365-102">Groups Collection (ADOX)</span></span>


<span data-ttu-id="b0365-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0365-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b0365-104">Содержит все хранимые объекты [групповой](group-object-adox.md) каталога или пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0365-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0365-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b0365-105">Remarks</span></span>

<span data-ttu-id="b0365-106">Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога.</span><span class="sxs-lookup"><span data-stu-id="b0365-106">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="b0365-107">Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="b0365-107">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="b0365-108">Метод [Append](append-method-adox-groups.md) для семейства сайтов **групп** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="b0365-108">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX.</span></span> <span data-ttu-id="b0365-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0365-109">You can:</span></span>

  - <span data-ttu-id="b0365-110">Добавление новой группы безопасности в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="b0365-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="b0365-111">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="b0365-111">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="b0365-112">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b0365-112">You can:</span></span>

  - <span data-ttu-id="b0365-113">Доступ к группы в семействе сайтов с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b0365-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="b0365-114">Возвращает число групп, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b0365-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="b0365-115">Удаление группы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="b0365-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="b0365-116">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="b0365-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b0365-117">Перед добавлением объекта <STRONG>группы</STRONG> в коллекцию <STRONG>групп</STRONG> объекта <STRONG>пользователя</STRONG> , объект <STRONG>группы</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекцию <STRONG>групп</STRONG> <STRONG>каталога</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b0365-117">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


