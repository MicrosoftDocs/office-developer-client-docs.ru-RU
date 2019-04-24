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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294423"
---
# <a name="datecreated-property-adox"></a>Свойство DateCreated (ADOX)


**Область применения**: Access 2013, Office 2013

Указывает дату создания объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **типа Variant** , определяющее созданную дату. Значение равно null, если **DateCreated** не поддерживается поставщиком.

## <a name="remarks"></a>Замечания

Для новых добавленных объектов свойство **DateCreated** имеет значение null. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md)необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции [представлений](views-collection-adox.md) или [процедур](procedures-collection-adox.md) для получения значений для свойства **DateCreated** .

