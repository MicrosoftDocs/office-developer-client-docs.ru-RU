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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287491"
---
# <a name="precision-property-adox"></a>Свойство Precision (ADOX)


**Область применения**: Access 2013, Office 2013

Указывает максимальную точность значений данных в столбце.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает **длинное** значение, которое является максимальной точностью значений данных в столбце, если свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) имеет числовой тип. **Точность** игнорируется для всех других типов данных.

## <a name="remarks"></a>Примечания

Значение по умолчанию — ноль (0).

Это свойство доступно только для чтения для объектов [Column](column-object-adox.md) , уже добавленных в коллекцию.

