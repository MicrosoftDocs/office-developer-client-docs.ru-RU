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

Указывает, как долго ждать при выполнении команды перед прекращением попытки и созданием ошибки.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long,** которое указывает в секундах, как долго ждать выполнения команды. Значение по умолчанию — 30.

## <a name="remarks"></a>Примечания

Используйте свойство **CommandTimeout** на объекте [Подключения](connection-object-ado.md) или объекте [Command,](command-object-ado.md) чтобы разрешить отмену вызова метода [Выполнения](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) из-за задержек из-за сетевого трафика или интенсивного использования сервера. Если интервал, установленный в свойстве **CommandTimeout,** завершается до завершения выполнения команды, возникает ошибка и ADO отменяет команду. Если задать свойство нулю, ADO будет ждать бесконечно, пока завершится выполнение. Убедитесь, что поставщик и источник данных, к которому вы пишете код, поддерживают функциональность **CommandTimeout.**

Параметр **CommandTimeout** для объекта **Подключения** не влияет на параметр **CommandTimeout** для объекта **Command** на том же **соединении;** то есть свойство **CommandTimeout** объекта **CommandTimeout** не наследует значение значения  **CommandTimeout** объекта Подключения.

В **объекте Подключение** свойство **CommandTimeout** сохраняется после открытия **подключения.**

