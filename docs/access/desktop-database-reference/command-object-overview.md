---
title: Command Object Overview
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1e6cd3b2ebea67fac7cef7e556038490b3eb9b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482927"
---
# <a name="command-object-overview"></a><span data-ttu-id="e27b9-102">Command Object Overview</span><span class="sxs-lookup"><span data-stu-id="e27b9-102">Command Object Overview</span></span>


<span data-ttu-id="e27b9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e27b9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e27b9-104">С помощью семейства сайтов, методы и свойства объекта **команды** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="e27b9-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="e27b9-105">Определение исполняемый текст команды (например, инструкции SQL или хранимую процедуру) с помощью свойства **CommandText** .</span><span class="sxs-lookup"><span data-stu-id="e27b9-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="e27b9-106">Определение запросы с параметрами и аргументами хранимую процедуру с помощью **параметра** объекты и коллекции **параметров** .</span><span class="sxs-lookup"><span data-stu-id="e27b9-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="e27b9-107">Выполнение команды и возврата объекта **набора записей** , если это необходимо, с помощью метода **Execute** .</span><span class="sxs-lookup"><span data-stu-id="e27b9-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="e27b9-108">Укажите тип команды с помощью свойства **CommandType** , прежде чем начать выполнение для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="e27b9-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="e27b9-109">Определяют, является ли поставщик сохраняет готовую (или скомпилированную) версию команды, прежде чем начать выполнение с помощью свойства **подготовленных** .</span><span class="sxs-lookup"><span data-stu-id="e27b9-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="e27b9-110">Задайте число секунд, поставщик будет ожидать команду, чтобы выполнить с помощью свойства **CommandTimeout** .</span><span class="sxs-lookup"><span data-stu-id="e27b9-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="e27b9-111">Связывание открытое подключение с помощью объекта **команды** , присвоив свойству **ActiveConnection** .</span><span class="sxs-lookup"><span data-stu-id="e27b9-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="e27b9-112">**Имя** свойства для идентификации объекта **команду** как метод на связанный объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="e27b9-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="e27b9-113">Передайте объект **команды** свойства **источника** **записей** для получения данных.</span><span class="sxs-lookup"><span data-stu-id="e27b9-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

