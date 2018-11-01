---
title: Коллекция столбцов (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a7abbf859162d527ac89c637022ce449219c235a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876528"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="1d2d3-102">Коллекция столбцов (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1d2d3-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="1d2d3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d2d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d2d3-104">Содержит все объекты [столбец](column-object-adox.md) таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="1d2d3-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2d3-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d2d3-105">Remarks</span></span>

<span data-ttu-id="1d2d3-106">Метод [Append](append-method-adox-columns.md) для коллекции **столбцов** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="1d2d3-106">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX.</span></span> <span data-ttu-id="1d2d3-107">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1d2d3-107">You can:</span></span>

  - <span data-ttu-id="1d2d3-108">Добавление нового столбца в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="1d2d3-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="1d2d3-109">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="1d2d3-109">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="1d2d3-110">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1d2d3-110">You can:</span></span>

  - <span data-ttu-id="1d2d3-111">Доступ к столбца в коллекции с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d2d3-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="1d2d3-112">Возвращает число столбцов, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d2d3-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="1d2d3-113">Удаление столбца из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="1d2d3-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="1d2d3-114">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="1d2d3-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="1d2d3-115">После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="1d2d3-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


