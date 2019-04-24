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
# <a name="command-object-overview"></a><span data-ttu-id="ac2aa-102">Обзор COM-объекта</span><span class="sxs-lookup"><span data-stu-id="ac2aa-102">Command object overview</span></span>

<span data-ttu-id="ac2aa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac2aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac2aa-104">С помощью коллекций, методов и свойств объекта **Command** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ac2aa-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="ac2aa-105">Определите исполняемый текст команды (например, инструкцию SQL или хранимую процедуру) с помощью свойства **CommandText** .</span><span class="sxs-lookup"><span data-stu-id="ac2aa-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="ac2aa-106">Определите параметризованные запросы или аргументы хранимой процедуры с помощью объектов **Parameter** и коллекции **Parameters** .</span><span class="sxs-lookup"><span data-stu-id="ac2aa-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="ac2aa-107">Выполнение команды и возврат объекта **Recordset** (при необходимости) с помощью метода **EXECUTE** .</span><span class="sxs-lookup"><span data-stu-id="ac2aa-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="ac2aa-108">Указание типа команды с помощью свойства **CommandType** перед выполнением для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="ac2aa-109">Следует ли поставщику сохранять подготовленную (или скомпилированную) версию команды перед выполнением с помощью свойства **preparedd** .</span><span class="sxs-lookup"><span data-stu-id="ac2aa-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="ac2aa-110">Задайте количество секунд, в течение которого поставщик будет ожидать выполнения команды, с помощью свойства **CommandTimeout** .</span><span class="sxs-lookup"><span data-stu-id="ac2aa-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="ac2aa-111">Свяжите открытое подключение с объектом **Command** , задав его свойство **ActiveConnection** .</span><span class="sxs-lookup"><span data-stu-id="ac2aa-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="ac2aa-112">Задайте свойство **Name** , чтобы оно определяло объект **Command** как метод в связанном объекте **Connection** .</span><span class="sxs-lookup"><span data-stu-id="ac2aa-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="ac2aa-113">Передайте объект **Command** свойству **Source** объекта **Recordset** для получения данных.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

