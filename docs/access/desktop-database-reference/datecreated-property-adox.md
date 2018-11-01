---
title: Свойство DateCreated (ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fea3e83f9a171a95eb844d9ba721039969804acf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876472"
---
# <a name="datecreated-property-adox"></a>Свойство DateCreated (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает дату создания объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **типа Variant** , определяющее Дата создания. Значение null, если **DateCreated** не поддерживается поставщиком.

## <a name="remarks"></a>Замечания

Свойство **DateCreated** имеет значение null для добавленного объектов. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateCreated** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .

