---
title: Коллекция столбцов (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1827fe11696e28871bdd03594ff0d7057c377dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296208"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="ab156-102">Коллекция столбцов (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ab156-102">Columns collection (ADOX)</span></span>


<span data-ttu-id="ab156-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab156-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab156-104">Содержит все [объекты Column](column-object-adox.md) таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="ab156-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab156-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab156-105">Remarks</span></span>

<span data-ttu-id="ab156-106">Метод [Приложения](append-method-adox-columns.md) для коллекции **Columns** уникален для ADOX.</span><span class="sxs-lookup"><span data-stu-id="ab156-106">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX.</span></span> <span data-ttu-id="ab156-107">Вы получаете перечисленные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="ab156-107">You can:</span></span>

  - <span data-ttu-id="ab156-108">Добавьте новый столбец в коллекцию с помощью метода **Приложения.**</span><span class="sxs-lookup"><span data-stu-id="ab156-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="ab156-109">Остальные свойства и методы являются стандартными для коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="ab156-109">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="ab156-110">Вы получаете перечисленные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="ab156-110">You can:</span></span>

  - <span data-ttu-id="ab156-111">Доступ к столбце в коллекции с [свойством Item.](item-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ab156-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="ab156-112">Возвращайте количество столбцов, содержащихся в коллекции, с [свойством Count.](count-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ab156-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="ab156-113">Удалите столбец из коллекции методом [Delete.](delete-method-adox-collections.md)</span><span class="sxs-lookup"><span data-stu-id="ab156-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="ab156-114">Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью [метода Обновления.](refresh-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ab156-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="ab156-115">Ошибка возникает при приложении  столбца к коллекции **Столбцы** индекса, если столбец не существует в таблице, которая уже примыкает к коллекции [Таблицы.](tables-collection-adox.md) [](index-object-adox.md)  [](table-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="ab156-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


