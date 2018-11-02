---
title: Коллекция Columns (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8278e43ba04047225f54171782c6a745a579595
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922302"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="420d4-102">Коллекция Columns (ADOX)</span><span class="sxs-lookup"><span data-stu-id="420d4-102">Columns collection (ADOX)</span></span>


<span data-ttu-id="420d4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="420d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="420d4-104">Содержит все объекты [столбец](column-object-adox.md) таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="420d4-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="420d4-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="420d4-105">Remarks</span></span>

<span data-ttu-id="420d4-106">Метод [Append](append-method-adox-columns.md) для коллекции **столбцов** является уникальным для ADOX.</span><span class="sxs-lookup"><span data-stu-id="420d4-106">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX.</span></span> <span data-ttu-id="420d4-107">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="420d4-107">You can:</span></span>

  - <span data-ttu-id="420d4-108">Добавление нового столбца в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="420d4-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="420d4-109">Остальные свойства и методы являются стандартными в семействах сайтов ADO.</span><span class="sxs-lookup"><span data-stu-id="420d4-109">The remaining properties and methods are standard to ADO collections.</span></span> <span data-ttu-id="420d4-110">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="420d4-110">You can:</span></span>

  - <span data-ttu-id="420d4-111">Доступ к столбца в коллекции с помощью свойства [элемента](item-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="420d4-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="420d4-112">Возвращает число столбцов, содержащихся в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="420d4-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="420d4-113">Удаление столбца из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .</span><span class="sxs-lookup"><span data-stu-id="420d4-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="420d4-114">Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="420d4-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="420d4-115">После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="420d4-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


