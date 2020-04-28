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

Указывает время ожидания при установлении подключения перед завершением попытки и генерацией ошибки.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Long** , которое указывает время ожидания открытия подключения (в секундах). Значение по умолчанию — 15.

## <a name="remarks"></a>Примечания

Используйте свойство **ConnectionTimeout** для объекта [Connection](connection-object-ado.md) , если задержка сетевого трафика или интенсивного использования сервера приводила к необходимости отказаться от попытки подключения. Если время из параметра свойства **ConnectionTimeout** проходит до открытия подключения, возникает ошибка, и ADO отменяет попытку. Если присвоить свойству нулевое значение, будет ожидать неопределенное время до открытия подключения. Убедитесь, что поставщик, с которым вы пишете код, поддерживает функцию **ConnectionTimeout** .

Свойство **ConnectionTimeout** доступно для чтения и записи, когда соединение закрывается и только для чтения при его открытии.

