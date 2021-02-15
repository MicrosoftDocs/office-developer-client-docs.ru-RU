---
title: Сохранение отфильтрованных и иерархических наборов записей
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1332d4348c993f94d8b2ee61280b8b35c02324c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287589"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Сохранение отфильтрованных и иерархических наборов записей


**Область применения**: Access 2013, Office 2013

Если свойство [Filter](filter-property-ado.md) действует для **объекта Recordset,** сохраняются только строки, доступные в фильтре. Если набор **записей является** иерархическим, то текущий потомок **Recordset** и его потомки сохраняются, включая родительский **набор записей.** Если вызван **метод Save** для child **Recordset,** то он и все его потомки сохраняются, а родительский — нет. Дополнительные сведения об иерархических **наборах записей** см. в главе [9 "Формирование данных".](chapter-9-data-shaping.md)


> [!NOTE]
> Некоторые ограничения применяются при сохранении иерархических **наборов записей** (фигур данных) в формате XML. Дополнительные сведения см. в [иерархических записях в XML.](hierarchical-recordsets-in-xml.md)


