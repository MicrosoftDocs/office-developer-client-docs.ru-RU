---
title: Сохранение иерархических наборов записей
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287582"
---
# <a name="persisting-hierarchical-recordsets"></a>Сохранение иерархических наборов записей

**Область применения**: Access 2013, Office 2013

Иерархический набор записей можно сохранить в файле в формате ADTG или XML, вызывая метод [Save.](save-method-ado.md)  Однако при сохранении иерархического наборов записей в формате XML применяются два  ограничения: невозможно сохранить в XML, если иерархический набор записей содержит ожидающих обновлений и нельзя сохранить параметризованный иерархический набор **записей.** 

Дополнительные сведения о поставщике формирования данных см. в службах формирования данных Майкрософт для [OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) и Data Shaping Service for OLE DB(OLE DB).

