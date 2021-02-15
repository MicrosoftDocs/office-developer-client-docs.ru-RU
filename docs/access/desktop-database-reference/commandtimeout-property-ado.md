---
title: Свойство CommandTimeout (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296131"
---
# <a name="commandtimeout-property-ado"></a>Свойство CommandTimeout (ADO)


**Область применения**: Access 2013, Office 2013

Указывает время ожидания выполнения команды перед прерыванием попытки и созданием ошибки.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **Long,** которое указывает (в секундах) время ожидания выполнения команды. Значение по умолчанию — 30.

## <a name="remarks"></a>Заметки

Используйте свойство **CommandTimeout** объекта [Connection](connection-object-ado.md) или [Command,](command-object-ado.md) чтобы разрешить отмену вызова метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) из-за задержек сетевого трафика или интенсивного использования сервера. Если интервал, установленный в свойстве **CommandTimeout,** завершает выполнение команды, возникает ошибка, и ADO отменяет команду. Если для свойства установлено нулевое значение, ADO будет ждать неопределенное время до завершения выполнения. Убедитесь, что поставщик и источник данных, в который вы пишете код, поддерживают **функции CommandTimeout.**

Параметр **CommandTimeout** для объекта **Connection** не влияет на параметр **CommandTimeout** для объекта **Command** в том же **соединении;** то есть свойство  **CommandTimeout** объекта Command не наследует значение значения **CommandTimeout** объекта Connection. 

В **объекте Connection** свойство **CommandTimeout** остается для чтения и записи после **открытия** подключения.

