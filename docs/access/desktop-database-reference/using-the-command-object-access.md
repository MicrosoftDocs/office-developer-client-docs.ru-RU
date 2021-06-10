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
# <a name="using-the-command-object-access"></a><span data-ttu-id="9096a-102">Использование объекта Command (Access)</span><span class="sxs-lookup"><span data-stu-id="9096a-102">Using the Command object (Access)</span></span>


<span data-ttu-id="9096a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9096a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9096a-104">После подключения к источнику данных необходимо выполнить запросы на него, чтобы получить наборы результатов.</span><span class="sxs-lookup"><span data-stu-id="9096a-104">After connecting to a data source, you need to execute requests against it to obtain result sets.</span></span> <span data-ttu-id="9096a-105">ADO инкапсулирует этот тип функций команды в **объекте Command.**</span><span class="sxs-lookup"><span data-stu-id="9096a-105">ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="9096a-106">Объект **Command** можно использовать для запроса любого типа операции у поставщика, если предположить, что поставщик может правильно интерпретировать строку команды.</span><span class="sxs-lookup"><span data-stu-id="9096a-106">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly.</span></span> <span data-ttu-id="9096a-107">Обычно поставщики данных запрашивают базу данных и возвращают записи в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="9096a-107">A common operation for data providers is to query a database and return records in a **Recordset** object.</span></span> <span data-ttu-id="9096a-108">**Recordset** s будет обсуждаться позже в этой и других главах; на данный момент думайте о них как о средствах для удержания и просмотра наборов результатов.</span><span class="sxs-lookup"><span data-stu-id="9096a-108">**Recordset** s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets.</span></span> <span data-ttu-id="9096a-109">Как и во многих объектах ADO, в зависимости от функциональности поставщика некоторые коллекции объектов **Command,** методы или свойства могут создавать ошибки при ссылке.</span><span class="sxs-lookup"><span data-stu-id="9096a-109">As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="9096a-110">Не всегда необходимо создавать объект **Command** для выполнения команды с источником данных.</span><span class="sxs-lookup"><span data-stu-id="9096a-110">It is not always necessary to create a **Command** object to execute a command against a data source.</span></span> <span data-ttu-id="9096a-111">Метод Execute **можно** использовать в **объекте Подключение** или метод **Open** на **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="9096a-111">You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object.</span></span> <span data-ttu-id="9096a-112">Однако следует использовать объект **Command,** если требуется повторное использование команды в коде или если вам необходимо передать подробные сведения о параметрах с командой.</span><span class="sxs-lookup"><span data-stu-id="9096a-112">However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command.</span></span> <span data-ttu-id="9096a-113">Эти сценарии подробно освещаются в этой главе.</span><span class="sxs-lookup"><span data-stu-id="9096a-113">These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="9096a-114">Некоторые команды могут возвращать результат, заданной как двоичный поток или в качестве единой записи, а не как набор записей, если он поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="9096a-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="9096a-115">Кроме того, некоторые команды не предназначены для возврата набора результатов вообще (например, запрос SQL обновления).</span><span class="sxs-lookup"><span data-stu-id="9096a-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="9096a-116">Однако в этой главе будет освещаться наиболее типичный сценарий: выполнение команд, возвращающих результаты в объект Recordset.</span><span class="sxs-lookup"><span data-stu-id="9096a-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="9096a-117">Дополнительные сведения о возвращении результатов в записи или Потоки см. в главе [10: Записи и Потоки.](chapter-10-records-and-streams.md)</span><span class="sxs-lookup"><span data-stu-id="9096a-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="9096a-118">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="9096a-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="9096a-119">Обзор COM-объекта</span><span class="sxs-lookup"><span data-stu-id="9096a-119">Command object overview</span></span>](command-object-overview.md)
- [<span data-ttu-id="9096a-120">Создание и выполнение простой команды</span><span class="sxs-lookup"><span data-stu-id="9096a-120">Creating and executing a simple command</span></span>](creating-and-executing-a-simple-command.md)
- [<span data-ttu-id="9096a-121">Параметры COM-объекта</span><span class="sxs-lookup"><span data-stu-id="9096a-121">Command object parameters</span></span>](command-object-parameters.md)
- [<span data-ttu-id="9096a-122">Вызов хранимой процедуры с помощью команды</span><span class="sxs-lookup"><span data-stu-id="9096a-122">Calling a stored procedure with a command</span></span>](calling-a-stored-procedure-with-a-command.md)
- [<span data-ttu-id="9096a-123">Именованные команды</span><span class="sxs-lookup"><span data-stu-id="9096a-123">Named commands</span></span>](named-commands.md)
