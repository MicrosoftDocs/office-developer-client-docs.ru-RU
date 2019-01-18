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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709329"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="25d98-102">С помощью объекта команды (доступ)</span><span class="sxs-lookup"><span data-stu-id="25d98-102">Using the Command object (Access)</span></span>


<span data-ttu-id="25d98-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25d98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25d98-104">После подключения к источнику данных, необходимые для выполнения запросов к нему для получения наборы результатов.</span><span class="sxs-lookup"><span data-stu-id="25d98-104">After connecting to a data source, you need to execute requests against it to obtain result sets.</span></span> <span data-ttu-id="25d98-105">ADO инкапсулирует этот тип функции команды в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="25d98-105">ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="25d98-106">Чтобы запросить любой тип операции у поставщика, при условии, что поставщик воспринимает строки команды должным образом, можно использовать объект **команды** .</span><span class="sxs-lookup"><span data-stu-id="25d98-106">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly.</span></span> <span data-ttu-id="25d98-107">Стандартная операция для поставщиков данных — для запросов к базе данных и возврата записей в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="25d98-107">A common operation for data providers is to query a database and return records in a **Recordset** object.</span></span> <span data-ttu-id="25d98-108">S **записей**будет описан далее в это, а также другие разделы; что их как наборы средств для хранения и просмотра результатов.</span><span class="sxs-lookup"><span data-stu-id="25d98-108">**Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets.</span></span> <span data-ttu-id="25d98-109">С помощью многие объекты ADO, в зависимости от функциональности поставщика, некоторые **команды** коллекций объектов, методов или свойств могут возникнуть ошибки при обращении к.</span><span class="sxs-lookup"><span data-stu-id="25d98-109">As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="25d98-110">Не всегда необходимо создать объект **команды** для выполнения команды в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="25d98-110">It is not always necessary to create a **Command** object to execute a command against a data source.</span></span> <span data-ttu-id="25d98-111">Метод **Execute** объекта **подключения** или метод **Open** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="25d98-111">You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object.</span></span> <span data-ttu-id="25d98-112">Тем не менее если вам потребуется повторно использовать команды в коде, или если нужно передать параметр detailed сведения с вашего команды следует использовать объект **команды** .</span><span class="sxs-lookup"><span data-stu-id="25d98-112">However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command.</span></span> <span data-ttu-id="25d98-113">Более подробно далее в этой главе рассматриваются следующие сценарии.</span><span class="sxs-lookup"><span data-stu-id="25d98-113">These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="25d98-114">Некоторые команды можно вернуть результирующего набора в виде двоичного потока или как одной записи, а не как набора записей, если это поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="25d98-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="25d98-115">Кроме того некоторые команды не предназначены для возврата любой набор всех результатов (например, обновление SQL query).</span><span class="sxs-lookup"><span data-stu-id="25d98-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="25d98-116">В этой главе будут рассмотрены наиболее типичные сценарии, однако: выполнение команд, которые возвращают результаты в объект набора записей.</span><span class="sxs-lookup"><span data-stu-id="25d98-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="25d98-117">Дополнительные сведения о возврате результатов в записей или потоки можно [Глава 10: записей и потоков](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="25d98-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="25d98-118">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="25d98-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="25d98-119">Обзор COM-объекта</span><span class="sxs-lookup"><span data-stu-id="25d98-119">Command object overview</span></span>](command-object-overview.md)
- [<span data-ttu-id="25d98-120">Создание и выполнение простой команды</span><span class="sxs-lookup"><span data-stu-id="25d98-120">Creating and executing a simple command</span></span>](creating-and-executing-a-simple-command.md)
- [<span data-ttu-id="25d98-121">Параметры COM-объекта</span><span class="sxs-lookup"><span data-stu-id="25d98-121">Command object parameters</span></span>](command-object-parameters.md)
- [<span data-ttu-id="25d98-122">Вызов хранимой процедуры с помощью команды</span><span class="sxs-lookup"><span data-stu-id="25d98-122">Calling a stored procedure with a command</span></span>](calling-a-stored-procedure-with-a-command.md)
- [<span data-ttu-id="25d98-123">Именованные команды</span><span class="sxs-lookup"><span data-stu-id="25d98-123">Named commands</span></span>](named-commands.md)
