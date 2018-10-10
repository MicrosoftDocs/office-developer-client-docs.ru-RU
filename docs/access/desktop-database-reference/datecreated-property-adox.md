---
title: DateCreated Property (ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 962c5e00eee3c58d2c02040869fdf1cb454af538
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482131"
---
# <a name="datecreated-property-adox"></a>DateCreated Property (ADOX)


**Применимо к**: Access 2013 | Office 2013

Указывает дату создания объекта.

## <a name="return-values"></a>Return Values

Возвращает значение **типа Variant** , определяющее Дата создания. Значение null, если **DateCreated** не поддерживается поставщиком.

## <a name="remarks"></a>Замечания

Свойство **DateCreated** имеет значение null для добавленного объектов. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateCreated** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .

