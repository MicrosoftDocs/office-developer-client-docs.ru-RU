---
title: Tables Collection (ADOX)
TOCTitle: Tables Collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43ca716cf03579c5c4cacf3f6b83a56d549b1433
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481620"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="69e11-102">Tables Collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="69e11-102">Tables Collection (ADOX)</span></span>


<span data-ttu-id="69e11-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="69e11-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="69e11-104">Содержит все объекты [в таблице](table-object-adox.md) каталога.</span><span class="sxs-lookup"><span data-stu-id="69e11-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="69e11-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="69e11-105">Remarks</span></span>

<span data-ttu-id="69e11-106">Метод [Append](append-method-adox-tables.md) для семейства сайтов **таблицы** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="69e11-106">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX.</span></span> <span data-ttu-id="69e11-107">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="69e11-107">You can:</span></span>

  - <span data-ttu-id="69e11-108">Добавление новой таблицы в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="69e11-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="69e11-109">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="69e11-109">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="69e11-110">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="69e11-110">You can:</span></span>

  - <span data-ttu-id="69e11-111">Доступ к таблице в коллекции с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="69e11-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="69e11-112">Возвращает количество таблиц, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="69e11-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="69e11-113">Удаление таблицы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="69e11-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="69e11-114">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="69e11-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="69e11-115">Некоторые поставщики возвращают другие объекты схемы, такие как представления, в коллекции таблиц.</span><span class="sxs-lookup"><span data-stu-id="69e11-115">Some providers may return other schema objects, such as a View, in the Tables collection.</span></span> <span data-ttu-id="69e11-116">Таким образом некоторые ADOX коллекции может содержать ссылки на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="69e11-116">Therefore, some ADOX collections may contain references to the same object.</span></span> <span data-ttu-id="69e11-117">Следует ли удалить объект из одного семейства сайтов, изменения не видны в другой коллекции, который ссылается на удаленный объект, пока не будет вызван метод Refresh в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="69e11-117">Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection.</span></span> <span data-ttu-id="69e11-118">Например с помощью поставщика OLE DB для Microsoft Jet, с коллекции таблиц возвращаются представления.</span><span class="sxs-lookup"><span data-stu-id="69e11-118">For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection.</span></span> <span data-ttu-id="69e11-119">При удалении представления необходимо обновить коллекции таблиц перед коллекции, будут изменены.</span><span class="sxs-lookup"><span data-stu-id="69e11-119">If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

