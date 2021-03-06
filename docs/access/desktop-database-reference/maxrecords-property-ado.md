---
title: Свойство MaxRecords (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289723"
---
# <a name="maxrecords-property-ado"></a>Свойство MaxRecords (ADO)


**Область применения**: Access 2013, Office 2013

Указывает максимальное количество записей, которые возвращаются в [набор записей](recordset-object-ado.md) из запроса.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long,** которое указывает максимальное количество возвращаемых записей. По умолчанию — ноль (без ограничений).

## <a name="remarks"></a>Примечания

Используйте **свойство MaxRecords,** чтобы ограничить количество записей, которые поставщик возвращает из источника данных. Значение по умолчанию для этого свойства нулевое, что означает, что поставщик возвращает все запрашиваемые записи.

Свойство **MaxRecords** считывало или записывало, когда **набор записей** закрыт и только для чтения, когда он открыт.

