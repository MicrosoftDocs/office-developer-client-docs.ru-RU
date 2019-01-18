---
title: Свойство DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712619"
---
# <a name="datecreated-property-adox"></a>Свойство DateCreated (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает дату создания объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **типа Variant** , определяющее Дата создания. Значение null, если **DateCreated** не поддерживается поставщиком.

## <a name="remarks"></a>Замечания

Свойство **DateCreated** имеет значение null для добавленного объектов. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateCreated** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .

