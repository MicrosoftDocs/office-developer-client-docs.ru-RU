---
title: Type Property (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bb4cebdb8b4aff1413ec60fe4ebb1e05931f6476
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306253"
---
# <a name="type-property-ado-stream"></a>Свойство Type (Stream в ADO)


**Область применения**: Access 2013, Office 2013

Указывает тип данных, которые хранятся в [потоке](stream-object-ado.md) (двоичный или текстовый).

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [стреамтипинум](streamtypeenum.md) , задающее тип данных, которые хранятся в объекте **Stream** . Значение по умолчанию — **адтипетекст**. Тем не менее, если двоичные данные изначально записываются в новый пустой **поток**, **Тип** изменится на **адтипебинари**.

## <a name="remarks"></a>Примечания

Свойство **Type** доступно для чтения и записи, только когда текущая позиция находится в начале **потока** ([position](position-property-ado.md) равно 0) и доступна только для чтения в любой другой позиции.

Свойство **Type** определяет методы, которые следует использовать для чтения и записи **потока**. Для текстовых **потоков**используйте [ReadText](readtext-method-ado.md) и [WriteText](writetext-method-ado.md). Для двоичных **потоков**используйте разрешение " [Чтение](read-method-ado.md) и [запись](write-method-ado.md)".

