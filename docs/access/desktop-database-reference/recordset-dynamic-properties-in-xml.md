---
title: Динамические свойства наборов записей в XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307660"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Динамические свойства наборов записей в XML

**Область применения**: Access 2013, Office 2013

Следующие свойства **поставщика Recordset** (из обработчик курсора клиента) в настоящее время сохраняются в формате XML:

- **AutoRecalc**
- **BatchSize**
- **CommandTimeout**
- **IRowsetChange**
- **IRowsetUpdate**
- **Reshape Name**
- **Resync Command**
- **Уникальный каталог**
- **Уникальная схема**
- **Уникальная таблица**
- **Обновление resync**
- **UpdateCriteria**


Эти свойства сохраняются в разделе схемы в качестве атрибутов определения элемента для **сохраняемого объекта Recordset.** Эти атрибуты определены в пространстве имен схемы наборов строк и должны иметь префикс "rs:".

## <a name="see-also"></a>См. также

- [Динамические свойства ADO](ado-dynamic-properties.md)
