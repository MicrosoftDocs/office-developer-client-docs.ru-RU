---
title: Объект Catalog (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d680c89f7188dafd216edf62bd07c80fa924a119
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026241"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="1a6b1-102">Объект Catalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1a6b1-102">Catalog object (ADOX)</span></span>


<span data-ttu-id="1a6b1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a6b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a6b1-104">Содержит коллекции ([таблицы](tables-collection-adox.md), [представления](views-collection-adox.md), [пользователей](users-collection-adox.md), [групп](groups-collection-adox.md)и [процедуры](procedures-collection-adox.md)), которые описывают каталога схемы из источника данных.</span><span class="sxs-lookup"><span data-stu-id="1a6b1-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6b1-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a6b1-105">Remarks</span></span>

<span data-ttu-id="1a6b1-106">Объект **каталога** можно изменить путем добавления или удаления объектов или путем изменения существующих объектов.</span><span class="sxs-lookup"><span data-stu-id="1a6b1-106">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects.</span></span> <span data-ttu-id="1a6b1-107">Некоторые поставщики могут не поддерживать все объекты **каталога** или может поддерживать только для просмотра сведений о схеме.</span><span class="sxs-lookup"><span data-stu-id="1a6b1-107">Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="1a6b1-108">С помощью свойства и методы объекта **каталога** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1a6b1-108">With the properties and methods of a **Catalog** object, you can:</span></span>

- <span data-ttu-id="1a6b1-109">Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-adox.md) объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="1a6b1-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

- <span data-ttu-id="1a6b1-110">Создайте новый каталог с помощью метода [Create](create-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6b1-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

- <span data-ttu-id="1a6b1-111">Определение владельцев объекты **каталога** с помощью методов [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) .</span><span class="sxs-lookup"><span data-stu-id="1a6b1-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span>

