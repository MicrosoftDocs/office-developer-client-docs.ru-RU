---
title: Свойство ConnectionTimeout (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab98e60e88a9685f138262a59a83f2b311c636da
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890934"
---
# <a name="connectiontimeout-property-ado"></a>Свойство ConnectionTimeout (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает время ожидания при установке соединения перед завершается и генерируется ошибка.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** , которое указывает, в секундах, время ожидания для подключения открыть. Значение по умолчанию — 15.

## <a name="remarks"></a>Замечания

Используйте свойство **ConnectionTimeout** на объект [подключения](connection-object-ado.md) Если использовать задержки сетевого трафика или высокая интенсивность операций сервера необходимо отменить попытку подключения. Если перед открытием подключения истечения времени от настройки свойства **ConnectionTimeout** , возникает ошибка, и ADO отменяет попытку. Если задать свойству присваивается значение 0, ADO будет ждать неограниченное время открытия подключения. Убедитесь, что поставщик, к которому написании кода поддерживает функциональную возможность **ConnectionTimeout** .

Свойство **ConnectionTimeout** — чтение и запись в случае подключения закрытой и только для чтения при открытии.

