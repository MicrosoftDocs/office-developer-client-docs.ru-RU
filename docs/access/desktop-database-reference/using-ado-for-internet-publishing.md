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



[Поставщик OLE DB для](the-ole-db-provider-for-internet-publishing.md) интернет-публикации показывает конкретный пример доступа к неоднородным данным с помощью ADO. Хотя примеры в этом разделе будут специфичеными для использования поставщика интернет-публикаций, принципы, продемонстрированные при использовании ADO с другими поставщиками, должны быть схожи с неоднородными данными, такими как поставщик в магазине электронной почты.

## <a name="urls"></a>URL-адреса

Единообразные локаторы ресурсов (URL-адреса) можно использовать в качестве альтернативы строкам подключения и тексту команд для указания источников данных и расположения файлов и каталогов. Url-адреса можно использовать с существующими объектами [Подключения](connection-object-ado.md) и **Recordset,** а также с объектами **Record** и **Stream.**

Дополнительные сведения об использовании URL-адресов см. в [url-адресах Absolute и Relative.](absolute-and-relative-urls.md)

## <a name="record-fields"></a>Поля записи

Различие между разнородными данными и однородными данными заключается в том, что для первой строки данных или Записи может быть другой набор столбцов или **полей.** Для однородных данных каждая строка имеет один и тот же набор столбцов. Дополнительные сведения о полях, определенных поставщику публикаций в Интернете, см. в журнале [Records and Provider-Supplied Fields.](records-and-provider-supplied-fields.md)

## <a name="appending-new-fields"></a>Приложение новых полей

Несколько объектов ADO были улучшены для работы в сочетании с объектами **Record** и **Stream.**

  - Метод [приложения](fields-collection-ado.md) коллекции [Fields,](append-method-ado.md) который создает и добавляет объект [Field](field-object-ado.md) в коллекцию, также может указать значение **Поля.**

  - Метод [Update](update-method-ado.md) завершает добавление или удаление полей в коллекцию.

  - В качестве ярлыка и альтернативы методу **Append** можно создать поля, просто назначив значение неопределяемой или ранее удаленной области.

## <a name="see-also"></a>См. также

- [Сценарии публикации в Интернете](internet-publishing-scenario.md)
