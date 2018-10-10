---
title: Persisting Filtered and Hierarchical Recordsets
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d29fe867933bdff93d064a95a4fc95c65e8605f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480903"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Persisting Filtered and Hierarchical Recordsets


**Применимо к**: Access 2013 | Office 2013

Если **записей**не свойство [фильтра](filter-property-ado.md) , будут сохранены только строки, доступных в группе фильтр. Если **записей** иерархических, дочерние текущего **набора записей** и его дочерние элементы сохраняются, включая родительского **набора записей**. Метод **Save** дочернего вызванный **записей** , дочерних и все его дочерние элементы сохраняются, но родительский не. Дополнительные сведения о иерархические **наборы записей**в разделе [Глава 9: формирования данных](chapter-9-data-shaping.md).


> [!NOTE]
> <P>Некоторые ограничения при сохранении иерархические <STRONG>наборы записей</STRONG> (данные фигуры) в формате XML. Для получения дополнительных сведений см <A href="hierarchical-recordsets-in-xml.md">Иерархические наборы записей в формате XML</A>.</P>


