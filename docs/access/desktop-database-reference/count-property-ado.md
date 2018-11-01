---
title: Свойство Count (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c710b02678940d898f910ef5215d879cd6ded163
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880861"
---
# <a name="count-property-ado"></a>Свойство Count (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает число объектов в коллекции.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** .

## <a name="remarks"></a>Замечания

Используйте свойство **Count** для определения количества объектов в данной коллекции.

Поскольку нумерация для элементов коллекции начинается с нуля, всегда должны кода циклов, начиная с нуля элемента и заканчивая значение свойства **Count** минус 1. Если используется Microsoft Visual Basic и хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , используйте **для** **каждого... Далее** команды.

Если свойство **Count** равно нулю, нет объектов в коллекции.

