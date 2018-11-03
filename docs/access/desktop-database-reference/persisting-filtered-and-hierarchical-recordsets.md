---
title: Сохранение фильтрацией и иерархические наборы записей
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13255bcd5cd40745a767b8aff9f49449b0127294
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946120"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Сохранение фильтрацией и иерархические наборы записей


**Применимо к**: Access 2013, Office 2013

Если **записей**не свойство [фильтра](filter-property-ado.md) , будут сохранены только строки, доступных в группе фильтр. Если **записей** иерархических, дочерние текущего **набора записей** и его дочерние элементы сохраняются, включая родительского **набора записей**. Метод **Save** дочернего вызванный **записей** , дочерних и все его дочерние элементы сохраняются, но родительский не. Дополнительные сведения о иерархические **наборы записей**в разделе [Глава 9: формирования данных](chapter-9-data-shaping.md).


> [!NOTE]
> Некоторые ограничения при сохранении иерархические **наборы записей** (данные фигуры) в формате XML. Для получения дополнительных сведений см [Иерархические наборы записей в формате XML](hierarchical-recordsets-in-xml.md).


