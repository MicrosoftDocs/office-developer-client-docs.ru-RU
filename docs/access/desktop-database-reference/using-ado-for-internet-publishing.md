---
title: Using ADO for Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae8341151c7bf7d90585794061647ba33a5c4ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305903"
---
# <a name="using-ado-for-internet-publishing"></a>Использование ADO для публикации в Интернете


**Область применения**: Access 2013, Office 2013



[Поставщик OLE DB для публикации](the-ole-db-provider-for-internet-publishing.md) в Интернете показывает конкретный пример доступа к разнородным данным с помощью ADO. Хотя в примерах в этом разделе используется поставщик публикации в Интернете, принципы, которые демонстрируются при использовании ADO с другими поставщиками, должны быть похожи на разнородные данные, такие как поставщик в хранилище электронной почты.

## <a name="urls"></a>URL-адреса

Url-адреса можно использовать в качестве альтернативы строкам подключения и тексту команды для указания источников данных и расположения файлов и каталогов. Вы можете использовать URL-адреса с существующими объектами [Connection](connection-object-ado.md) и **Recordset,** а также с объектами **Record** и **Stream.**

Дополнительные сведения об использовании URL-адресов см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)

## <a name="record-fields"></a>Поля записей

Различие между разнородными и однородными данными состоит в том, что для первой строки данных или записи может быть разный набор столбцов или полей.  Для однородных данных каждая строка имеет одинаковый набор столбцов. Дополнительные сведения о полях, характерных для поставщика интернет-публикации, см. в Provider-Supplied ["Записи" и "Provider-Supplied".](records-and-provider-supplied-fields.md)

## <a name="appending-new-fields"></a>Appending New Fields

Несколько объектов ADO были улучшены для работы в сочетании с объектами **Record** и **Stream.**

  - Метод [Append коллекции](append-method-ado.md) [Fields,](fields-collection-ado.md) который создает и добавляет объект [Field](field-object-ado.md) в коллекцию, также может указывать значение **поля.**

  - Метод [Update](update-method-ado.md) завершает добавление или удаление полей в коллекцию.

  - В качестве ярлыка и альтернативы методу **Append** можно создать поля, просто назначив значение неопределененным или ранее удаленным полям.

## <a name="see-also"></a>См. также

- [Темы сценария публикации в Интернете](internet-publishing-scenario.md)
