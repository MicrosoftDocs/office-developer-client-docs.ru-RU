---
title: Свойство NumericScale (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1a15f78463ca0ff6e690b600b9cdca7cc194c7
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025961"
---
# <a name="numericscale-property-adox"></a>Свойство NumericScale (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает масштаб числовое значение в столбце.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение в **байтах** , масштаб значений данных в столбце, когда [Тип](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) свойства — **adNumeric** или **adDecimal**. **NumericScale** игнорируется для всех остальных типов данных.

## <a name="remarks"></a>Примечания

Значение по умолчанию — нуль (0).

**NumericScale** доступен только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.

