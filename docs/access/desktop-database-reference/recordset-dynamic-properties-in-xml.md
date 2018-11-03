---
title: Динамические свойства наборов записей в XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36069ec0e8e9020bc70ef1ea72ce25f4461c6487
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946960"
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