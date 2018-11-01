---
title: Свойство NumericScale (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11696e379fe618f07a6087eee26ba21a2d27b3e5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890920"
---
# <a name="numericscale-property-adox"></a>Свойство NumericScale (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает масштаб числовое значение в столбце.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение в **байтах** , масштаб значений данных в столбце, когда [Тип](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) свойства — **adNumeric** или **adDecimal**. **NumericScale** игнорируется для всех остальных типов данных.

## <a name="remarks"></a>Замечания

Значение по умолчанию — нуль (0).

**NumericScale** доступен только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.

