---
title: Объект Table (ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19f30bec624a43bc1b821d8bef01afa166b0c544
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026430"
---
# <a name="table-object-adox"></a><span data-ttu-id="8b500-102">Объект Table (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8b500-102">Table object (ADOX)</span></span>

<span data-ttu-id="8b500-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b500-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b500-104">Представляет таблицу базы данных, включая столбцов, индексов и ключи.</span><span class="sxs-lookup"><span data-stu-id="8b500-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b500-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b500-105">Remarks</span></span>

<span data-ttu-id="8b500-106">Следующий код создает новую **таблицу**.</span><span class="sxs-lookup"><span data-stu-id="8b500-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="8b500-107">С помощью свойств и коллекций объектов **в таблице** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b500-107">With the properties and collections of a **Table** object, you can:</span></span>

- <span data-ttu-id="8b500-108">Определение таблицы с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b500-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="8b500-109">Определите тип таблицы с помощью свойства [типа](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) .</span><span class="sxs-lookup"><span data-stu-id="8b500-109">Determine the type of table with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) property.</span></span>

- <span data-ttu-id="8b500-110">Доступ к столбцам базы данных таблицы с помощью коллекции [столбцов](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b500-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8b500-111">Доступ к индексов таблицы с помощью коллекции [индексов](indexes-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b500-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8b500-112">Доступ к разделам таблицы с набором [разделов](keys-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b500-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8b500-113">Укажите [каталог](catalog-object-adox.md) , который несет ответственность за таблицы с помощью свойства [ParentCatalog](parentcatalog-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b500-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

- <span data-ttu-id="8b500-114">Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b500-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

- <span data-ttu-id="8b500-115">Доступа к свойствам конкретного поставщика в таблице с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8b500-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="8b500-116">Поставщик данных может поддерживает все свойства объектов **в таблице** .</span><span class="sxs-lookup"><span data-stu-id="8b500-116">Your data provider may not support all properties of **Table** objects.</span></span> <span data-ttu-id="8b500-117">Если выбрать значение для свойства, которое не поддерживает поставщик, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="8b500-117">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="8b500-118">Для новых объектов **в таблице** ошибка возникает, когда объект добавляется в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="8b500-118">For new **Table** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="8b500-119">Для существующих объектов ошибка возникает, когда для свойства.</span><span class="sxs-lookup"><span data-stu-id="8b500-119">For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="8b500-120">При создании объектов **в таблице** , наличие значения по умолчанию для необязательные свойства не гарантирует, что ваш поставщик поддерживает свойство.</span><span class="sxs-lookup"><span data-stu-id="8b500-120">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="8b500-121">Для получения дополнительных сведений о свойствах ваш поставщик поддерживает обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b500-121">For more information about which properties your provider supports, see your provider documentation.</span></span>

