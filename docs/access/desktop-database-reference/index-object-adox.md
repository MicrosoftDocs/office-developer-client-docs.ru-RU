---
title: Объект Index (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5bc2eeaf4d26c957abb67780fe2f5d0df8f73049
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026178"
---
# <a name="index-object-adox"></a><span data-ttu-id="0b1d2-102">Объект Index (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0b1d2-102">Index object (ADOX)</span></span>

<span data-ttu-id="0b1d2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b1d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b1d2-104">Представляет индекс из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-104">Represents an index from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1d2-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b1d2-105">Remarks</span></span>

<span data-ttu-id="0b1d2-106">Следующий код создает новый **индекса**.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-106">The following code creates a new **Index**:</span></span>

`Dim obj As New Index`

<span data-ttu-id="0b1d2-107">С помощью свойств и коллекций объекта **индекса** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-107">With the properties and collections of an **Index** object, you can:</span></span>

- <span data-ttu-id="0b1d2-108">Определение индекса с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-108">Identify the index with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="0b1d2-109">Доступ к столбцам базы данных индекса в коллекции [столбцов](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-109">Access the database columns of the index with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="0b1d2-110">Укажите, должны ли быть уникальными со свойством [Unique](unique-property-adox.md) разделов индекса.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-110">Specify whether the index keys must be unique with the [Unique](unique-property-adox.md) property.</span></span>

- <span data-ttu-id="0b1d2-111">Укажите, является ли индекс первичный ключ для таблицы с помощью свойства [PrimaryKey](primarykey-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-111">Specify whether the index is the primary key for a table with the [PrimaryKey](primarykey-property-adox.md) property.</span></span>

- <span data-ttu-id="0b1d2-112">Укажите, будет ли записи, которые имеют значение null, значения в полях индекса записи индекса с помощью свойства [IndexNulls](indexnulls-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-112">Specify whether records that have null values in their index fields have index entries with the [IndexNulls](indexnulls-property-adox.md) property.</span></span>

- <span data-ttu-id="0b1d2-113">Укажите, является ли индекс кластерные со свойством [Clustered](clustered-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-113">Specify whether the index is clustered with the [Clustered](clustered-property-adox.md) property.</span></span>

- <span data-ttu-id="0b1d2-114">Доступа к свойствам поставщика индекса в коллекции [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-114">Access provider-specific index properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="0b1d2-115">После добавления [столбцов](column-object-adox.md) в коллекцию **столбцов** **индекса** , если **Столбец** не существует в объекте [таблицы](table-object-adox.md) уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-115">An error will occur when appending a [Column](column-object-adox.md) to the **Columns** collection of an **Index** if the **Column** does not exist in a [Table](table-object-adox.md) object already appended to the [Tables](tables-collection-adox.md) collection.</span></span>

<span data-ttu-id="0b1d2-116">Поставщик данных может поддерживает все свойства объектов **индекса** .</span><span class="sxs-lookup"><span data-stu-id="0b1d2-116">Your data provider may not support all properties of **Index** objects.</span></span> <span data-ttu-id="0b1d2-117">Если выбрать значение для свойства, которое не поддерживается поставщиком, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-117">An error will occur if you have set a value for a property that is not supported by the provider.</span></span> <span data-ttu-id="0b1d2-118">Для новых объектов **индекса** ошибка возникает при объект добавляется к коллекции.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-118">For new **Index** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="0b1d2-119">Для существующих объектов ошибка возникает, когда для свойства.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-119">For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="0b1d2-120">При создании объектов **индекса** , наличие значения по умолчанию для необязательные свойства не гарантирует, что ваш поставщик поддерживает свойство.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-120">When creating **Index** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="0b1d2-121">Для получения дополнительных сведений о свойствах ваш поставщик поддерживает обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="0b1d2-121">For more information about which properties your provider supports, see your provider documentation.</span></span>

