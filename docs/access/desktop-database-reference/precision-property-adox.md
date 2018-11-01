---
title: Свойство точности (ADOX)
TOCTitle: Precision Property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f61359c368202c1820c713f5842eef3102c3f3d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868415"
---
# <a name="precision-property-adox"></a>Свойство точности (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает максимальное точность значений данных в столбце.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение типа **Long** , является максимальной точности значений данных в столбце, если свойство [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) является числовым типом. **Точность** игнорируется для всех остальных типов данных.

## <a name="remarks"></a>Замечания

Значение по умолчанию — нуль (0).

Это свойство доступно только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.

