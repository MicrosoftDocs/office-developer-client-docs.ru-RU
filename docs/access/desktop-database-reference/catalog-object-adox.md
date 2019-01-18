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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714908"
---
# <a name="catalog-object-adox"></a>Объект Catalog (ADOX)


**Применимо к**: Access 2013, Office 2013

Содержит коллекции ([таблицы](tables-collection-adox.md), [представления](views-collection-adox.md), [пользователей](users-collection-adox.md), [групп](groups-collection-adox.md)и [процедуры](procedures-collection-adox.md)), которые описывают каталога схемы из источника данных.

## <a name="remarks"></a>Замечания

Объект **каталога** можно изменить путем добавления или удаления объектов или путем изменения существующих объектов. Некоторые поставщики могут не поддерживать все объекты **каталога** или может поддерживать только для просмотра сведений о схеме.

С помощью свойства и методы объекта **каталога** можно выполнить следующие действия.

- Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-adox.md) объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.

- Создайте новый каталог с помощью метода [Create](create-method-adox.md) .

- Определение владельцев объекты **каталога** с помощью методов [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) .

