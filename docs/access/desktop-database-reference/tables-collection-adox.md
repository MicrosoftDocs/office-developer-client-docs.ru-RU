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
# <a name="tables-collection-adox"></a><span data-ttu-id="2028d-102">Коллекция Tables (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2028d-102">Tables collection (ADOX)</span></span>


<span data-ttu-id="2028d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2028d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2028d-104">Содержит все объекты [Table](table-object-adox.md) каталога.</span><span class="sxs-lookup"><span data-stu-id="2028d-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="2028d-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="2028d-105">Remarks</span></span>

<span data-ttu-id="2028d-106">Метод [append](append-method-adox-tables.md) для коллекции **Tables** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="2028d-106">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX.</span></span> <span data-ttu-id="2028d-107">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2028d-107">You can:</span></span>

  - <span data-ttu-id="2028d-108">Добавление новой таблицы в коллекцию с помощью метода **append** .</span><span class="sxs-lookup"><span data-stu-id="2028d-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="2028d-109">Остальные свойства и методы являются стандартными для коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="2028d-109">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="2028d-110">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2028d-110">You can:</span></span>

  - <span data-ttu-id="2028d-111">Доступ к таблице в коллекции со свойством [Item](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2028d-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="2028d-112">Возвращает количество таблиц, хранящихся в коллекции, со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2028d-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="2028d-113">Удаление таблицы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="2028d-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="2028d-114">Обновление объектов в коллекции в соответствии с схемой текущей базы данных с помощью метода [Refresh](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2028d-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="2028d-115">Некоторые поставщики могут возвращать другие объекты схемы, например представление, в коллекции Tables.</span><span class="sxs-lookup"><span data-stu-id="2028d-115">Some providers may return other schema objects, such as a View, in the Tables collection.</span></span> <span data-ttu-id="2028d-116">Таким образом, некоторые коллекции ADOX могут содержать ссылки на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="2028d-116">Therefore, some ADOX collections may contain references to the same object.</span></span> <span data-ttu-id="2028d-117">Если вы удалите объект из одной коллекции, это изменение не будет отображаться в другой коллекции, ссылающейся на удаленный объект, пока не будет вызван метод Refresh в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2028d-117">Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection.</span></span> <span data-ttu-id="2028d-118">Например, при использовании поставщика OLE DB для Microsoft Jet представления возвращаются с помощью коллекции Tables.</span><span class="sxs-lookup"><span data-stu-id="2028d-118">For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection.</span></span> <span data-ttu-id="2028d-119">При удалении представления необходимо обновить коллекцию Tables, прежде чем коллекция будет отражать изменение.</span><span class="sxs-lookup"><span data-stu-id="2028d-119">If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

