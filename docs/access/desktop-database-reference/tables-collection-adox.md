---
title: Коллекция Tables (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314051"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="cbdb8-102">Коллекция Tables (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cbdb8-102">Tables collection (ADOX)</span></span>


<span data-ttu-id="cbdb8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbdb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbdb8-104">Содержит все [объекты Table](table-object-adox.md) каталога.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbdb8-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="cbdb8-105">Remarks</span></span>

<span data-ttu-id="cbdb8-106">Метод [Append](append-method-adox-tables.md) для коллекции **Tables** уникален для ADOX.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-106">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX.</span></span> <span data-ttu-id="cbdb8-107">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-107">You can:</span></span>

  - <span data-ttu-id="cbdb8-108">Добавьте новую таблицу в коллекцию с помощью **метода Append.**</span><span class="sxs-lookup"><span data-stu-id="cbdb8-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="cbdb8-109">Остальные свойства и методы являются стандартными для коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-109">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="cbdb8-110">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-110">You can:</span></span>

  - <span data-ttu-id="cbdb8-111">Доступ к таблице в коллекции с помощью [свойства Item.](item-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="cbdb8-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="cbdb8-112">Возвращает количество таблиц, содержащихся в коллекции, со свойством [Count.](count-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="cbdb8-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="cbdb8-113">Удалите таблицу из коллекции с помощью метода [Delete.](delete-method-adox-collections.md)</span><span class="sxs-lookup"><span data-stu-id="cbdb8-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="cbdb8-114">Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью метода [Refresh.](refresh-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="cbdb8-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="cbdb8-115">Некоторые поставщики могут возвращать другие объекты схемы, например View, в коллекции Tables.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-115">Some providers may return other schema objects, such as a View, in the Tables collection.</span></span> <span data-ttu-id="cbdb8-116">Поэтому некоторые коллекции ADOX могут содержать ссылки на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-116">Therefore, some ADOX collections may contain references to the same object.</span></span> <span data-ttu-id="cbdb8-117">Если удалить объект из одной коллекции, изменение не будет видно в другой коллекции, которая ссылается на удаленный объект, пока в коллекции не будет вызван метод Refresh.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-117">Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection.</span></span> <span data-ttu-id="cbdb8-118">Например, при поставщике OLE DB для Microsoft Jet представления возвращаются вместе с коллекцией Tables.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-118">For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection.</span></span> <span data-ttu-id="cbdb8-119">При сбросе представления необходимо обновить коллекцию Tables, прежде чем коллекция отразит изменение.</span><span class="sxs-lookup"><span data-stu-id="cbdb8-119">If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

