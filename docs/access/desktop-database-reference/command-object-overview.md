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
# <a name="command-object-overview"></a><span data-ttu-id="569a7-102">Обзор COM-объекта</span><span class="sxs-lookup"><span data-stu-id="569a7-102">Command object overview</span></span>

<span data-ttu-id="569a7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="569a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="569a7-104">С помощью коллекций, методов и свойств объекта **Command** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="569a7-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="569a7-105">Определите исполняемый текст команды (например, SQL или сохраненную процедуру) с помощью свойства **CommandText.**</span><span class="sxs-lookup"><span data-stu-id="569a7-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="569a7-106">Определите параметризированные запросы или аргументы хранимых процедур с помощью объектов **Parameter** и **коллекции Параметры.**</span><span class="sxs-lookup"><span data-stu-id="569a7-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="569a7-107">Выполните команду и верни объект **Recordset,** если это необходимо, с помощью метода **Execute.**</span><span class="sxs-lookup"><span data-stu-id="569a7-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="569a7-108">Укажите тип команды с помощью свойства **CommandType** перед выполнением для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="569a7-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="569a7-109">Управление сохранением подготовленной (или компилировать) версии команды перед выполнением с помощью свойства **Prepared.**</span><span class="sxs-lookup"><span data-stu-id="569a7-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="569a7-110">Установите количество секунд, которое поставщик будет ждать выполнения команды с помощью свойства **CommandTimeout.**</span><span class="sxs-lookup"><span data-stu-id="569a7-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="569a7-111">Связать открытое подключение с **объектом Command,** установив его свойство **ActiveConnection.**</span><span class="sxs-lookup"><span data-stu-id="569a7-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="569a7-112">Установите свойство **Name,** чтобы определить **объект Command** как метод на связанном **объекте Подключения.**</span><span class="sxs-lookup"><span data-stu-id="569a7-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="569a7-113">**Передай объект Command** свойству **Source** **recordset** для получения данных.</span><span class="sxs-lookup"><span data-stu-id="569a7-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

