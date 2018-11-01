---
title: Свойство MaxRecords (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d66a26cffb14220670643c5b6b5aafe94e8fcb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870088"
---
# <a name="maxrecords-property-ado"></a>Свойство MaxRecords (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает максимальное число записей для возврата [набора записей](recordset-object-ado.md) из запроса.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** , указывающее максимальное число возвращаемых записей. Значение по умолчанию — 0 (без ограничений).

## <a name="remarks"></a>Замечания

Свойство **MaxRecords** максимальное число записей, которые поставщик возвращает из источника данных. По умолчанию этого свойства равно нулю, что означает, что поставщик возвращает все запрошенные записей.

Свойство **MaxRecords** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.

