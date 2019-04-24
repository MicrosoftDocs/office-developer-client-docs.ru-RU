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

Указывает время ожидания при выполнении команды перед завершением попытки и генерацией ошибки.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Long** , которое указывает время ожидания выполнения команды (в секундах). Значение по умолчанию — 30.

## <a name="remarks"></a>Замечания

Используйте свойство **CommandTimeout** для объекта [подключения](connection-object-ado.md) или объекта [Command](command-object-ado.md) , чтобы разрешить отмену вызова метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) из-за задержки сетевого трафика или интенсивного использования сервера. Если интервал, заданный в свойстве **CommandTimeout** , проходит до завершения выполнения команды, возникает ошибка, и ADO отменяет команду. Если присвоить свойству значение ноль, ADO будет ожидать неопределенное время, пока выполнение не будет завершено. Убедитесь, что поставщик и источник данных, с которыми вы пишете код, поддерживают функцию **CommandTimeout** .

Параметр **CommandTimeout** для объекта **Connection** не оказывает никакого действия для параметра **CommandTimeout** для объекта **Command** в том же соединении; **** то есть, свойство **CommandTimeout** объекта **Command** не наследует значение значения **CommandTimeout** объекта **Connection** .

Для объекта **Connection** свойство **CommandTimeout** остается доступно для чтения и записи после открытия **подключения** .

