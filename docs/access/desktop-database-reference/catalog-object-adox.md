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
# <a name="catalog-object-adox"></a>Объект Catalog (ADOX)


**Область применения**: Access 2013, Office 2013

Содержит коллекции[(таблицы,](tables-collection-adox.md) [представления,](views-collection-adox.md) [пользователи,](users-collection-adox.md) [группы](groups-collection-adox.md)и процедуры), [](procedures-collection-adox.md)которые описывают каталог схемы источника данных.

## <a name="remarks"></a>Заметки

Объект каталога **можно изменить,** добавив или удалив объекты или изменяя существующие объекты. Некоторые поставщики могут поддерживать не все объекты **каталога** или только просмотр сведений о схеме.

С помощью свойств и методов объекта **Catalog** можно:

- Откройте каталог, задав для свойства [ActiveConnection](activeconnection-property-adox.md) объект подключения [ADO](connection-object-ado.md) или допустимую строку подключения.

- Создайте каталог с помощью метода [Create.](create-method-adox.md)

- Определите владельцев объектов в **каталоге** с помощью методов [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox)

