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

Указывает тип данных, содержащихся в [Потоке](stream-object-ado.md) (двоичный или текстовый).

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение [StreamTypeEnum,](streamtypeenum.md) которое указывает тип данных, содержащихся в **объекте Stream.** По умолчанию значение **adTypeText**. Однако если двоичные данные изначально записаны в новый пустой **поток,** **тип** будет изменен на **adTypeBinary.**

## <a name="remarks"></a>Примечания

Свойство **Type** считыв или записываю только в [](position-property-ado.md) том случае, если текущее положение находится в начале потока **(положение** 0) и только для чтения в любом другом расположении.

Свойство **Type** определяет, какие методы следует использовать для чтения и записи **потока.** Для **текстовых Потоки** используйте [ReadText](readtext-method-ado.md) и [WriteText](writetext-method-ado.md). Для двоичных **Потоки** используйте [чтение](read-method-ado.md) и [записи](write-method-ado.md).

