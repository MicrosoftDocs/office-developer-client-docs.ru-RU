---
title: Свойство Count (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295473"
---
# <a name="count-property-ado"></a>Свойство Count (ADO)


**Область применения**: Access 2013, Office 2013

Указывает количество объектов в коллекции.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **длинное** значение.

## <a name="remarks"></a>Заметки

Используйте свойство **Count,** чтобы определить, сколько объектов находится в заданной коллекции.

Так как нуминг для членов коллекции начинается с нуля, необходимо всегда кодировать циклы, начиная с нулевого члена и заканчивая значением свойства **Count** минус 1. Если вы используете Microsoft Visual Basic и хотите перенабывать члены коллекции, не проверяя свойство **Count,** используйте свойство **For** **Each... Следующая** команда.

Если свойство **Count** имеет нулевое значение, в коллекции нет объектов.

