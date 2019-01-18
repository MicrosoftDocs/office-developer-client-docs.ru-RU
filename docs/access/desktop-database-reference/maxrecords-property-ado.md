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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709357"
---
# <a name="maxrecords-property-ado"></a>Свойство MaxRecords (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает максимальное число записей для возврата [набора записей](recordset-object-ado.md) из запроса.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** , указывающее максимальное число возвращаемых записей. Значение по умолчанию — 0 (без ограничений).

## <a name="remarks"></a>Замечания

Свойство **MaxRecords** максимальное число записей, которые поставщик возвращает из источника данных. По умолчанию этого свойства равно нулю, что означает, что поставщик возвращает все запрошенные записей.

Свойство **MaxRecords** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.

