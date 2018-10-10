---
title: Count Property (ADO)
TOCTitle: Count Property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad02d854a560e3fa99bf7454c97083e88638c520
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481376"
---
# <a name="count-property-ado"></a>Count Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает число объектов в коллекции.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** .

## <a name="remarks"></a>Замечания

Используйте свойство **Count** для определения количества объектов в данной коллекции.

Поскольку нумерация для элементов коллекции начинается с нуля, всегда должны кода циклов, начиная с нуля элемента и заканчивая значение свойства **Count** минус 1. Если используется Microsoft Visual Basic и хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , используйте **для** **каждого... Далее** команды.

Если свойство **Count** равно нулю, нет объектов в коллекции.

