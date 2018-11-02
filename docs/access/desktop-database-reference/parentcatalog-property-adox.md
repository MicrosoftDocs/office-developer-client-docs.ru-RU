---
title: Свойство ParentCatalog (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bbeed0283eaf7982d037cfe7bf4773db9a8c03b5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928455"
---
# <a name="parentcatalog-property-adox"></a>Свойство ParentCatalog (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает каталог родительской таблицы или столбца для предоставления доступа к свойствам конкретного поставщика.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает объект [каталога](catalog-object-adox.md) . Параметру **ParentCatalog** open **каталога** позволяет получить доступ к свойствам конкретного поставщика перед добавлением таблицы или столбца в коллекцию **каталога** .

## <a name="remarks"></a>Примечания

Некоторые поставщики данных Разрешить значения свойства от поставщика для записи только при создании (если таблицы или столбца добавляется к коллекции **каталога** ). Для доступа к этим свойствам перед добавлением этих объектов **каталога**, укажите **каталога** в свойстве **ParentCatalog** сначала.

Когда таблицы или столбца добавляется другой **каталог** чем **ParentCatalog**возникает ошибка.

