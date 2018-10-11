---
title: Recordset Dynamic Properties in XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4193220e450c59e7293ed6befa37d8da23801f27
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480104"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Recordset Dynamic Properties in XML


**Применимо к**: Access 2013 | Office 2013

## <a name="recordset-dynamic-properties-in-xml"></a>Recordset Dynamic Properties in XML

Следующие свойства от поставщика **набора записей** (от обработчика курсор клиента) в настоящее время, сохраняются в формате XML:

  - **Обновление повторной синхронизации**

  - **Уникальная таблица**

  - **Уникальный схемы**

  - **Уникальный каталога**

  - **Команда синхронизации**

  - **IRowsetChange**

  - **IRowsetUpdate**

  - **CommandTimeout**

  - **Размер пакета**

  - **UpdateCriteria**

  - **Изменить форму имя**

  - **AutoRecalc**

Эти свойства сохраняются в разделе схемы как атрибуты определения элемента для **набора записей** , сохраняется. Эти атрибуты определены в пространстве имен схемы строк и должен иметь префикс «rs:».

