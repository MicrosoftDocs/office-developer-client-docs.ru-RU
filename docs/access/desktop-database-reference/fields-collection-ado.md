---
title: Коллекция Fields (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292575"
---
# <a name="fields-collection-ado"></a>Коллекция Fields (ADO)


**Область применения**: Access 2013, Office 2013

Содержит все [объекты Field](field-object-ado.md) объекта [Recordset](recordset-object-ado.md) или [Record.](record-object-ado.md)

## <a name="remarks"></a>Заметки

Объект **Recordset** имеет коллекцию **Fields,** которая состоит из **объектов Field.** Каждый объект **Field** соответствует столбцу в **наборе записей.** Можно заполнить коллекцию **Fields** перед открытием **recordset,** вызывая метод [Refresh](refresh-method-ado.md) в коллекции.

> [!NOTE]
> Более **подробное описание** использования объектов Field см. в разделе "Объект **Field".**

Коллекция **Fields** содержит метод [Append,](append-method-ado.md) который временно создает и добавляет объект **Field** в коллекцию, и метод **Update,** который завершает все добавления или удаления.

Объект **Record** имеет два особых поля, которые можно индексировать с помощью [констант FieldEnum.](fieldenum.md) Одна константа имеет доступ к полю, содержащим поток по умолчанию для записи, а другой к полю, содержащей абсолютную строку URL-адреса **для записи.**

Некоторые поставщики (например, поставщик [Microsoft OLE DB для](microsoft-ole-db-provider-for-internet-publishing.md)публикации в Интернете) могут заполнить коллекцию **Fields** подмножество доступных полей для record **или** **Recordset.** Другие поля не будут добавлены в коллекцию до тех пор, пока они не будут сначала ссылаться по имени или индексироваться кодом.

При попытке ссылаться на несущестующие поля по имени новый объект **Field** будет [](status-property-ado-field.md) примещаться к коллекции **Fields** со статусом **adFieldPendingInsert.** При вызове [update](update-method-ado.md)ADO создаст новое поле в источнике данных, если это разрешено поставщиком.

