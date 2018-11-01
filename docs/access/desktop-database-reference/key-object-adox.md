---
title: Объект ключа (ADOX - ссылки для настольных баз данных Access)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2edda6dfe7dd9ec28f3eb4cb11714d59806c80e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871362"
---
# <a name="key-object-adox"></a><span data-ttu-id="50c04-102">Объект ключа (ADOX)</span><span class="sxs-lookup"><span data-stu-id="50c04-102">Key Object (ADOX)</span></span>


<span data-ttu-id="50c04-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50c04-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50c04-104">Представляет основной, внешний или уникальное ключевое поле из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="50c04-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="50c04-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="50c04-105">Remarks</span></span>

<span data-ttu-id="50c04-106">Следующий код создает новый **ключ**.</span><span class="sxs-lookup"><span data-stu-id="50c04-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="50c04-107">С помощью свойств и коллекций объекта **ключа** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="50c04-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="50c04-108">Определите ключ с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="50c04-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="50c04-109">Определите, является ли ключ основной, внешний или уникальные со свойством [типа](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="50c04-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="50c04-110">Доступ к столбцам базы данных ключа в коллекции [столбцов](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="50c04-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="50c04-111">Укажите имя связанной таблицы с помощью свойства [RelatedTable](relatedtable-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="50c04-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="50c04-112">Определите действие, выполняемое на удаление или обновление основного ключа с помощью свойства [DeleteRule](deleterule-property-adox.md) и [UpdateRule](updaterule-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="50c04-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

