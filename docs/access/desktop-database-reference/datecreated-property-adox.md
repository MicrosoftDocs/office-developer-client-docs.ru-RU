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

Возвращает значение **Variant,** указывав дату создания. Значение null, если **DateCreated** не поддерживается поставщиком.

## <a name="remarks"></a>Примечания

Свойство **DateCreated** является null для вновь пристроенных объектов. После придания [](view-object-adox.md) нового представления или процедуры [необходимо](procedure-object-adox.md)вызвать [](views-collection-adox.md) метод [](procedures-collection-adox.md) [Обновления](refresh-method-ado.md) коллекции Просмотры или Процедуры для получения значений для **свойства DateCreated.**

