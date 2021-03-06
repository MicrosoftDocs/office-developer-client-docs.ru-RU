---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b89d292d86035e565ad18413062274dfbfc74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312028"
---
# <a name="using-the-command-object-access"></a>Использование объекта Command (Access)


**Область применения**: Access 2013, Office 2013

После подключения к источнику данных необходимо выполнить запросы на него, чтобы получить наборы результатов. ADO инкапсулирует этот тип функций команды в **объекте Command.**

Объект **Command** можно использовать для запроса любого типа операции у поставщика, если предположить, что поставщик может правильно интерпретировать строку команды. Обычно поставщики данных запрашивают базу данных и возвращают записи в **объекте Recordset.** **Recordset** s будет обсуждаться позже в этой и других главах; на данный момент думайте о них как о средствах для удержания и просмотра наборов результатов. Как и во многих объектах ADO, в зависимости от функциональности поставщика некоторые коллекции объектов **Command,** методы или свойства могут создавать ошибки при ссылке.

Не всегда необходимо создавать объект **Command** для выполнения команды с источником данных. Метод Execute **можно** использовать в **объекте Подключение** или метод **Open** на **объекте Recordset.** Однако следует использовать объект **Command,** если требуется повторное использование команды в коде или если вам необходимо передать подробные сведения о параметрах с командой. Эти сценарии подробно освещаются в этой главе.

> [!NOTE]
> Некоторые команды могут возвращать результат, заданной как двоичный поток или в качестве единой записи, а не как набор записей, если он поддерживается поставщиком. Кроме того, некоторые команды не предназначены для возврата набора результатов вообще (например, запрос SQL обновления). Однако в этой главе будет освещаться наиболее типичный сценарий: выполнение команд, возвращающих результаты в объект Recordset. Дополнительные сведения о возвращении результатов в записи или Потоки см. в главе [10: Записи и Потоки.](chapter-10-records-and-streams.md)

В этой статье содержатся следующие разделы:

- [Обзор COM-объекта](command-object-overview.md)
- [Создание и выполнение простой команды](creating-and-executing-a-simple-command.md)
- [Параметры COM-объекта](command-object-parameters.md)
- [Вызов хранимой процедуры с помощью команды](calling-a-stored-procedure-with-a-command.md)
- [Именованные команды](named-commands.md)
