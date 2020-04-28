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

Если свойство [Filter](filter-property-ado.md) применяется для объекта **Recordset**, сохраняются только те строки, которые доступны в фильтре. Если объект **Recordset** является иерархический, сохраняются текущий дочерний **набор записей** и его дочерние элементы, в том числе родительский **набор записей**. При вызове метода **Save** дочернего объекта **Recordset** , дочерний объект и все его дочерние элементы сохраняются, а родитель — нет. Дополнительные сведения о иерархических **наборах записей**приведены в [главе 9: формирование данных](chapter-9-data-shaping.md).


> [!NOTE]
> При сохранении иерархических **наборов записей** (форм данных) в формате XML применяются некоторые ограничения. Более подробную информацию можно узнать [в статье иерархические наборы записей в XML](hierarchical-recordsets-in-xml.md).


