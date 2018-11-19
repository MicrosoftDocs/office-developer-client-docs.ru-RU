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
# <a name="catalog-object-adox"></a>Объект Catalog (ADOX)


**Применимо к**: Access 2013, Office 2013

Содержит коллекции ([таблицы](tables-collection-adox.md), [представления](views-collection-adox.md), [пользователей](users-collection-adox.md), [групп](groups-collection-adox.md)и [процедуры](procedures-collection-adox.md)), которые описывают каталога схемы из источника данных.

## <a name="remarks"></a>Примечания

Объект **каталога** можно изменить путем добавления или удаления объектов или путем изменения существующих объектов. Некоторые поставщики могут не поддерживать все объекты **каталога** или может поддерживать только для просмотра сведений о схеме.

С помощью свойства и методы объекта **каталога** можно выполнить следующие действия.

- Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-adox.md) объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.

- Создайте новый каталог с помощью метода [Create](create-method-adox.md) .

- Определение владельцев объекты **каталога** с помощью методов [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) .

