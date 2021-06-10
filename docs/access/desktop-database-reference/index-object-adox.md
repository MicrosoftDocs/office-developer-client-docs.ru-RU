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
# <a name="index-object-adox"></a><span data-ttu-id="1c010-102">Объект Index (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1c010-102">Index object (ADOX)</span></span>

<span data-ttu-id="1c010-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c010-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c010-104">Представляет индекс из таблицы баз данных.</span><span class="sxs-lookup"><span data-stu-id="1c010-104">Represents an index from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c010-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c010-105">Remarks</span></span>

<span data-ttu-id="1c010-106">Следующий код создает новый **индекс:**</span><span class="sxs-lookup"><span data-stu-id="1c010-106">The following code creates a new **Index**:</span></span>

`Dim obj As New Index`

<span data-ttu-id="1c010-107">С свойствами и коллекциями объекта **Index** можно:</span><span class="sxs-lookup"><span data-stu-id="1c010-107">With the properties and collections of an **Index** object, you can:</span></span>

- <span data-ttu-id="1c010-108">Определите индекс с [свойством Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1c010-108">Identify the index with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="1c010-109">Доступ к столбцам базы данных индекса с помощью коллекции [Столбцы.](columns-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1c010-109">Access the database columns of the index with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="1c010-110">Укажите, должны ли клавиши индекса быть уникальными с [свойством Unique.](unique-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1c010-110">Specify whether the index keys must be unique with the [Unique](unique-property-adox.md) property.</span></span>

- <span data-ttu-id="1c010-111">Укажите, является ли индекс основным ключом для таблицы с [свойством PrimaryKey.](primarykey-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1c010-111">Specify whether the index is the primary key for a table with the [PrimaryKey](primarykey-property-adox.md) property.</span></span>

- <span data-ttu-id="1c010-112">Укажите, имеют ли записи с значениями null в своих полях индекса записи с [свойством IndexNulls.](indexnulls-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1c010-112">Specify whether records that have null values in their index fields have index entries with the [IndexNulls](indexnulls-property-adox.md) property.</span></span>

- <span data-ttu-id="1c010-113">Укажите, кластерит ли индекс с [свойством Clustered.](clustered-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1c010-113">Specify whether the index is clustered with the [Clustered](clustered-property-adox.md) property.</span></span>

- <span data-ttu-id="1c010-114">Доступ к свойствам индекса для конкретного поставщика с [коллекцией свойств.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1c010-114">Access provider-specific index properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="1c010-115">Ошибка возникает при приложении [](column-object-adox.md) столбца к коллекции **Столбцов**  индекса, если столбец не существует в объекте [Table,](table-object-adox.md) который уже придан в коллекцию [Таблицы.](tables-collection-adox.md) </span><span class="sxs-lookup"><span data-stu-id="1c010-115">An error will occur when appending a [Column](column-object-adox.md) to the **Columns** collection of an **Index** if the **Column** does not exist in a [Table](table-object-adox.md) object already appended to the [Tables](tables-collection-adox.md) collection.</span></span>

<span data-ttu-id="1c010-116">Поставщик данных может не поддерживать все свойства объектов **Index.**</span><span class="sxs-lookup"><span data-stu-id="1c010-116">Your data provider may not support all properties of **Index** objects.</span></span> <span data-ttu-id="1c010-117">Ошибка будет возникать, если вы установили значение для свойства, которое не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1c010-117">An error will occur if you have set a value for a property that is not supported by the provider.</span></span> <span data-ttu-id="1c010-118">Для новых **объектов Index** ошибка возникает при приложении объекта к коллекции.</span><span class="sxs-lookup"><span data-stu-id="1c010-118">For new **Index** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="1c010-119">Для существующих объектов ошибка возникает при настройке свойства.</span><span class="sxs-lookup"><span data-stu-id="1c010-119">For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="1c010-120">При создании **объектов Index** наличие соответствующего значения по умолчанию для необязательных свойств не гарантирует, что поставщик поддерживает свойство.</span><span class="sxs-lookup"><span data-stu-id="1c010-120">When creating **Index** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="1c010-121">Дополнительные сведения о свойствах, поддерживаемых поставщиком, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="1c010-121">For more information about which properties your provider supports, see your provider documentation.</span></span>

