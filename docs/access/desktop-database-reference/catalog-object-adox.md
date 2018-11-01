---
title: Объект каталога (ADOX)
TOCTitle: Catalog Object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d1be720b8c3791830a4258d6241466ba596d85e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887658"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="51d6f-102">Объект каталога (ADOX)</span><span class="sxs-lookup"><span data-stu-id="51d6f-102">Catalog Object (ADOX)</span></span>


<span data-ttu-id="51d6f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51d6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51d6f-104">Содержит коллекции ([таблицы](tables-collection-adox.md), [представления](views-collection-adox.md), [пользователей](users-collection-adox.md), [групп](groups-collection-adox.md)и [процедуры](procedures-collection-adox.md)), которые описывают каталога схемы из источника данных.</span><span class="sxs-lookup"><span data-stu-id="51d6f-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d6f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="51d6f-105">Remarks</span></span>

<span data-ttu-id="51d6f-106">Объект **каталога** можно изменить путем добавления или удаления объектов или путем изменения существующих объектов.</span><span class="sxs-lookup"><span data-stu-id="51d6f-106">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects.</span></span> <span data-ttu-id="51d6f-107">Некоторые поставщики могут не поддерживать все объекты **каталога** или может поддерживать только для просмотра сведений о схеме.</span><span class="sxs-lookup"><span data-stu-id="51d6f-107">Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="51d6f-108">С помощью свойства и методы объекта **каталога** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="51d6f-108">With the properties and methods of a **Catalog** object, you can:</span></span>

  - <span data-ttu-id="51d6f-109">Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-adox.md) объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="51d6f-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

  - <span data-ttu-id="51d6f-110">Создайте новый каталог с помощью метода [Create](create-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="51d6f-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

  - <span data-ttu-id="51d6f-111">Определение владельцев объекты **каталога** с помощью методов [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="51d6f-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) methods.</span></span>

