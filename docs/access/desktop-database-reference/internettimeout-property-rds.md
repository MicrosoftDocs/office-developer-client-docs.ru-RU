---
title: Свойство InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291243"
---
# <a name="internettimeout-property-rds"></a>Свойство InternetTimeout (RDS)


**Область применения**: Access 2013, Office 2013

Указывает количество миллисекунд, которые нужно ждать до времени ожидания запроса.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long,** которое представляет число миллисекунд, прежде чем запрос будет отсутвить время.

## <a name="remarks"></a>Примечания

Это свойство применяется только к запросам, отправленным с протоколами HTTP или HTTPS.

Выполнение запросов в трехуровневой среде может занять несколько минут. Используйте это свойство, чтобы указать дополнительное время для длительных запросов.

