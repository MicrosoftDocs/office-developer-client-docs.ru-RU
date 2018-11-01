---
title: Свойства динамической записей в формате XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48714b9178e99cfd4ccf7738f3ad4a342572fdfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884263"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Свойства динамической записей в формате XML


**Применимо к**: Access 2013, Office 2013

## <a name="recordset-dynamic-properties-in-xml"></a>Свойства динамической записей в формате XML

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

