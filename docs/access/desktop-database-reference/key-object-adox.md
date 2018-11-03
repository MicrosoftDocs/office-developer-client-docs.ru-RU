---
title: Объект ключа (ADOX - ссылки для настольных баз данных Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11bd05c4959ba1f3e1819e482ce311fc798bf0e6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929834"
---
# <a name="key-object-adox"></a><span data-ttu-id="4ca98-102">Объект Key (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4ca98-102">Key object (ADOX)</span></span>


<span data-ttu-id="4ca98-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ca98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ca98-104">Представляет основной, внешний или уникальное ключевое поле из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="4ca98-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca98-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ca98-105">Remarks</span></span>

<span data-ttu-id="4ca98-106">Следующий код создает новый **ключ**.</span><span class="sxs-lookup"><span data-stu-id="4ca98-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="4ca98-107">С помощью свойств и коллекций объекта **ключа** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4ca98-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="4ca98-108">Определите ключ с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca98-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="4ca98-109">Определите, является ли ключ основной, внешний или уникальные со свойством [типа](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="4ca98-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="4ca98-110">Доступ к столбцам базы данных ключа в коллекции [столбцов](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca98-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="4ca98-111">Укажите имя связанной таблицы с помощью свойства [RelatedTable](relatedtable-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca98-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="4ca98-112">Определите действие, выполняемое на удаление или обновление основного ключа с помощью свойства [DeleteRule](deleterule-property-adox.md) и [UpdateRule](updaterule-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca98-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

