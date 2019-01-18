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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712836"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Динамические свойства наборов записей в XML

**Применимо к**: Access 2013, Office 2013

Следующие свойства от поставщика **набора записей** (от обработчика курсор клиента) в настоящее время, сохраняются в формате XML:

- **AutoRecalc**
- **Размер пакета**
- **CommandTimeout**
- **IRowsetChange**
- **IRowsetUpdate**
- **Изменить форму имя**
- **Команда синхронизации**
- **Уникальный каталога**
- **Уникальный схемы**
- **Уникальная таблица**
- **Обновление повторной синхронизации**
- **UpdateCriteria**


Эти свойства сохраняются в разделе схемы как атрибуты определения элемента для **набора записей** , сохраняется. Эти атрибуты определены в пространстве имен схемы строк и должен иметь префикс «rs:».

## <a name="see-also"></a>См. также

- [Динамические свойства ADO](ado-dynamic-properties.md)
