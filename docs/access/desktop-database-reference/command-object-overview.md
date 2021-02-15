---
title: Обзор COM-объекта
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c7697d4ae8b830afb53eee10e7dd59a7dc8db4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296166"
---
# <a name="command-object-overview"></a>Обзор COM-объекта

**Область применения**: Access 2013, Office 2013

С помощью коллекций, методов и свойств объекта **Command** можно сделать следующее:

  - Определите исполняемый текст команды (например, SQL или хранимую процедуру) с помощью свойства **CommandText.**

  - Определите параметризованные запросы или хранимые аргументы процедуры с помощью объектов **Parameter** и коллекции **Parameters.**

  - Выполните команду и при необходимости вернете объект **Recordset** с помощью метода **Execute.**

  - Укажите тип команды с помощью свойства **CommandType** перед выполнением для оптимизации производительности.

  - Уберите, сохраняет ли поставщик подготовленную (или скомпилную) версию команды перед выполнением с помощью свойства **Prepared.**

  - Установите время в секундах, в течение которое поставщик будет ждать выполнения команды с помощью свойства **CommandTimeout.**

  - Связывание открытого подключения с **объектом Command** путем установки его свойства **ActiveConnection.**

  - Установите свойство **Name,** чтобы определить **объект Command** в качестве метода для связанного **объекта Connection.**

  - **Передав объект Command** свойству **Source** объекта **Recordset,** чтобы получить данные.

