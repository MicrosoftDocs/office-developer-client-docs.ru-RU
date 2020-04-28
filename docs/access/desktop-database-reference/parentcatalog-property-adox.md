---
title: Свойство ParentCatalog (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287785"
---
# <a name="parentcatalog-property-adox"></a>Свойство ParentCatalog (ADOX)


**Область применения**: Access 2013, Office 2013

Задает родительский каталог таблицы или столбца для предоставления доступа к свойствам, зависящим от поставщика.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает объект [Catalog](catalog-object-adox.md) . Установка **ParentCatalog** в открытый **Каталог** позволяет получить доступ к свойствам, зависящим от поставщика, перед добавлением таблицы или столбца в коллекцию **каталогов** .

## <a name="remarks"></a>Примечания

Некоторые поставщики данных позволяют записывать значения свойств, специфичные для поставщика, только при создании (при добавлении таблицы или столбца в коллекцию **каталогов** ). Чтобы получить доступ к этим свойствам перед добавлением этих объектов в **Каталог**, сначала укажите **Каталог** в свойстве **ParentCatalog** .

Ошибка возникает, когда таблица или столбец добавляются в каталог, отличный от **каталога** **ParentCatalog**.

