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

Указывает, сколько времени нужно подождать, пока будет устанавливаться подключение, прежде чем завершить попытку и создать ошибку.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **Long,** которое указывает (в секундах) время ожидания открытия подключения. Значение по умолчанию — 15.

## <a name="remarks"></a>Заметки

Используйте свойство **ConnectionTimeout** объекта [Connection,](connection-object-ado.md) если задержка сетевого трафика или интенсивное использование сервера делают необходимым отказаться от попытки подключения. Если время, задаваемого параметром свойства **ConnectionTimeout** до открытия подключения, уже зависает, возникает ошибка, и ADO отменяет попытку. Если для свойства установлено нулевое значение, ADO будет ждать неопределенное время, пока не будет открыто подключение. Убедитесь, что поставщик, которому вы пишете код, поддерживает **функции ConnectionTimeout.**

Свойство **ConnectionTimeout** считывать и записывать при закрытии подключения и только для чтения, когда оно открыто.

