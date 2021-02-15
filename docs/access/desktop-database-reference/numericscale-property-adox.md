---
title: Свойство NumericScale (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288520"
---
# <a name="numericscale-property-adox"></a>Свойство NumericScale (ADOX)


**Область применения**: Access 2013, Office 2013

Указывает масштаб числимого значения в столбце.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение **byte,** которое является масштабом значений данных в столбце, если свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) является **adNumeric** или **adDecimal**. **NumericScale** игнорируется для всех других типов данных.

## <a name="remarks"></a>Заметки

Значение по умолчанию — ноль (0).

**NumericScale** доступно только для чтения для объектов [Column,](column-object-adox.md) которые уже были приданы к коллекции.

