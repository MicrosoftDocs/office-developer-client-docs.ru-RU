---
title: Объект Catalog (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8cc0237d1419c3aba818d54811f1dbdeeaa441c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296572"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="7d743-102">Объект Catalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7d743-102">Catalog object (ADOX)</span></span>


<span data-ttu-id="7d743-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d743-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d743-104">Содержит коллекции ([таблицы](tables-collection-adox.md), [представления](views-collection-adox.md), [Пользователи](users-collection-adox.md), [группы](groups-collection-adox.md)и [процедуры](procedures-collection-adox.md)), описывающие Каталог схемы источника данных.</span><span class="sxs-lookup"><span data-stu-id="7d743-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d743-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d743-105">Remarks</span></span>

<span data-ttu-id="7d743-106">Вы можете изменить объект **Catalog** , добавив или удалив объекты или изменив существующие объекты.</span><span class="sxs-lookup"><span data-stu-id="7d743-106">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects.</span></span> <span data-ttu-id="7d743-107">Некоторые поставщики могут не поддерживать все объекты **каталога** или могут поддерживать только сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="7d743-107">Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="7d743-108">С помощью свойств и методов объекта **Catalog** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7d743-108">With the properties and methods of a **Catalog** object, you can:</span></span>

- <span data-ttu-id="7d743-109">Откройте каталог, задав для свойства [ActiveConnection](activeconnection-property-adox.md) объект [подключения](connection-object-ado.md) ADO или допустимую строку подключения.</span><span class="sxs-lookup"><span data-stu-id="7d743-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

- <span data-ttu-id="7d743-110">Создайте новый каталог с помощью метода [CREATE](create-method-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7d743-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

- <span data-ttu-id="7d743-111">Определите владельцев объектов в **каталоге** с помощью методов [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) .</span><span class="sxs-lookup"><span data-stu-id="7d743-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span>

