---
title: InternetTimeout Property (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd0fdc8f64207e1233ac56812ef009da865ce01a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603464"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout Property (RDS)


**Применимо к**: Access 2013 | Office 2013

Указывает время в миллисекундах для ожидания, по истечении времени ожидания запроса.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение типа **Long** , представляющее номер (в миллисекундах) перед запрос будет завершен.

## <a name="remarks"></a>Замечания

Это свойство применяется только к запросы, отправленные по протоколам HTTP или HTTPS.

Запросы в среде трехуровневой может занять несколько минут для выполнения. Это свойство используется для указания дополнительного времени для длительным запросам.

