---
title: Свойство DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 344b193b3ab8d6800fcf81b6bb2d184b1104f9d3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923102"
---
# <a name="datecreated-property-adox"></a>Свойство DateCreated (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает дату создания объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **типа Variant** , определяющее Дата создания. Значение null, если **DateCreated** не поддерживается поставщиком.

## <a name="remarks"></a>Примечания

Свойство **DateCreated** имеет значение null для добавленного объектов. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateCreated** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .

