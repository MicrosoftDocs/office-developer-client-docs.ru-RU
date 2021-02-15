---
title: Объект Index (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02d12fffa2c766425054e344e9f7d9d7a22cb517
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291777"
---
# <a name="index-object-adox"></a><span data-ttu-id="9e5a7-102">Объект Index (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9e5a7-102">Index object (ADOX)</span></span>

<span data-ttu-id="9e5a7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e5a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e5a7-104">Представляет индекс из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e5a7-104">Represents an index from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5a7-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="9e5a7-105">Remarks</span></span>

<span data-ttu-id="9e5a7-106">Следующий код создает новый **индекс:**</span><span class="sxs-lookup"><span data-stu-id="9e5a7-106">The following code creates a new **Index**:</span></span>

`Dim obj As New Index`

<span data-ttu-id="9e5a7-107">С помощью свойств и коллекций объекта **Index** можно:</span><span class="sxs-lookup"><span data-stu-id="9e5a7-107">With the properties and collections of an **Index** object, you can:</span></span>

- <span data-ttu-id="9e5a7-108">Определите индекс с помощью [свойства Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e5a7-108">Identify the index with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="9e5a7-109">Доступ к столбцам базы данных индекса с помощью коллекции [Columns.](columns-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e5a7-109">Access the database columns of the index with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="9e5a7-110">Укажите, должны ли ключи индекса быть уникальными с помощью [свойства Unique.](unique-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e5a7-110">Specify whether the index keys must be unique with the [Unique](unique-property-adox.md) property.</span></span>

- <span data-ttu-id="9e5a7-111">Укажите, является ли индекс первичным ключом для таблицы со [свойством PrimaryKey.](primarykey-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e5a7-111">Specify whether the index is the primary key for a table with the [PrimaryKey](primarykey-property-adox.md) property.</span></span>

- <span data-ttu-id="9e5a7-112">Укажите, имеют ли записи со значениями NULL в своих полях индекса записи индекса со свойством [IndexNulls.](indexnulls-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e5a7-112">Specify whether records that have null values in their index fields have index entries with the [IndexNulls](indexnulls-property-adox.md) property.</span></span>

- <span data-ttu-id="9e5a7-113">Укажите, кластеризация ли индекса с помощью [кластерного](clustered-property-adox.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="9e5a7-113">Specify whether the index is clustered with the [Clustered](clustered-property-adox.md) property.</span></span>

- <span data-ttu-id="9e5a7-114">Доступ к свойствам индекса для определенного поставщика с помощью коллекции [Properties.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9e5a7-114">Access provider-specific index properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="9e5a7-115">Ошибка будет возникать при [](column-object-adox.md) приложении столбца к  коллекции **Columns** индекса, если столбец не существует в [объекте Table,](table-object-adox.md) который уже был придан коллекции [Tables.](tables-collection-adox.md) </span><span class="sxs-lookup"><span data-stu-id="9e5a7-115">An error will occur when appending a [Column](column-object-adox.md) to the **Columns** collection of an **Index** if the **Column** does not exist in a [Table](table-object-adox.md) object already appended to the [Tables](tables-collection-adox.md) collection.</span></span>

<span data-ttu-id="9e5a7-116">Поставщик данных может поддерживать не все свойства объектов **Index.**</span><span class="sxs-lookup"><span data-stu-id="9e5a7-116">Your data provider may not support all properties of **Index** objects.</span></span> <span data-ttu-id="9e5a7-117">Ошибка возникает, если вы установили значение для свойства, которое не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="9e5a7-117">An error will occur if you have set a value for a property that is not supported by the provider.</span></span> <span data-ttu-id="9e5a7-118">Для новых **объектов Index** ошибка возникает, когда объект будет appended к коллекции.</span><span class="sxs-lookup"><span data-stu-id="9e5a7-118">For new **Index** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="9e5a7-119">Для существующих объектов ошибка возникает при установке свойства.</span><span class="sxs-lookup"><span data-stu-id="9e5a7-119">For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="9e5a7-120">При создании **объектов Index** наличие соответствующего значения по умолчанию для необязательного свойства не гарантирует, что ваш поставщик поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="9e5a7-120">When creating **Index** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="9e5a7-121">Дополнительные сведения о свойствах, поддерживаемые поставщиком, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e5a7-121">For more information about which properties your provider supports, see your provider documentation.</span></span>

