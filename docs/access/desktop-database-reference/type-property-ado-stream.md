---
title: Свойство Type (ADO потока)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1a5c9c69b5de6fbdf57efedf9724ae71ac151b7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945532"
---
# <a name="type-property-ado-stream"></a>Свойство Type (объект Stream в ADO)


**Применимо к**: Access 2013, Office 2013

Указывает тип данных, содержащихся в [потоке](stream-object-ado.md) (двоичный или текст).

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает [StreamTypeEnum](streamtypeenum.md) значение, задающее тип данных, содержащихся в объекте **потока** . Значение по умолчанию — **adTypeText**. Тем не менее если изначально двоичные данные записываются новый, пустой **поток**, **Тип** будет изменено на **adTypeBinary**.

## <a name="remarks"></a>Примечания

Является ли данное свойство **Тип** чтения и записи только в том случае, если текущее положение находится в начале **потока** ([положение](position-property-ado.md) — 0) и только для чтения в любом другом месте.

Свойство **Type** определяет, какие методы можно использовать для чтения и записи в **поток**. Для текста, **потоки**используйте [ReadText](readtext-method-ado.md) и [WriteText](writetext-method-ado.md). Для двоичных **потоков**используйте [чтения](read-method-ado.md) и [записи](write-method-ado.md).

