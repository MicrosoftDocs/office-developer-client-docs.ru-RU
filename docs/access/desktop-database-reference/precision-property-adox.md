---
title: Свойство Precision (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f05f6880a9599421189519f263cfb27bf1432325
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726164"
---
# <a name="precision-property-adox"></a>Свойство Precision (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает максимальное точность значений данных в столбце.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение типа **Long** , является максимальной точности значений данных в столбце, если свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) является числовым типом. **Точность** игнорируется для всех остальных типов данных.

## <a name="remarks"></a>Замечания

Значение по умолчанию — нуль (0).

Это свойство доступно только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.

