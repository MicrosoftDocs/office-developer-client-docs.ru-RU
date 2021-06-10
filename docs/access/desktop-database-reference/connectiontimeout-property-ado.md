---
title: Свойство ConnectionTimeout (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295704"
---
# <a name="connectiontimeout-property-ado"></a>Свойство ConnectionTimeout (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, как долго ждать при создании подключения перед прекращением попытки и созданием ошибки.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long,** которое за секунды указывает, как долго ждать открытия подключения. Значение по умолчанию — 15.

## <a name="remarks"></a>Примечания

Используйте свойство **ConnectionTimeout** на [объекте Подключения,](connection-object-ado.md) если задержки с сетевым трафиком или использованием тяжелых серверов делают необходимым отказаться от попытки подключения. Если время, задаваемого параметром **свойства ConnectionTimeout,** уходящего до открытия подключения, возникает ошибка, и ADO отменяет попытку. Если значение свойства установлено до нуля, ADO будет ждать до открытия подключения бесконечно. Убедитесь, что поставщик, которому вы пишете код, поддерживает функциональность **ConnectionTimeout.**

Свойство **ConnectionTimeout** считыв или записывалось при закрытии подключения и только для чтения, когда оно открыто.

