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
# <a name="using-the-command-object-access"></a><span data-ttu-id="ff6b7-102">Использование объекта Command (Access)</span><span class="sxs-lookup"><span data-stu-id="ff6b7-102">Using the Command object (Access)</span></span>


<span data-ttu-id="ff6b7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff6b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff6b7-104">После подключения к источнику данных необходимо выполнить для него запросы на получение наборов результатов.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-104">After connecting to a data source, you need to execute requests against it to obtain result sets.</span></span> <span data-ttu-id="ff6b7-105">ADO инкапсулирует этот тип функции команды в объекте **Command** .</span><span class="sxs-lookup"><span data-stu-id="ff6b7-105">ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="ff6b7-106">С помощью объекта **Command** можно запросить любой тип операции у поставщика, предполагая, что поставщик может правильно интерпретировать командную строку.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-106">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly.</span></span> <span data-ttu-id="ff6b7-107">Распространенной операцией для поставщиков данных является запрос к базе данных и возврат записей в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ff6b7-107">A common operation for data providers is to query a database and return records in a **Recordset** object.</span></span> <span data-ttu-id="ff6b7-108">**Наборы записей**, которые будут обсуждаться далее в этой и других главах; пока что они будут рассматривать их как инструменты для хранения и просмотра наборов результатов.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-108">**Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets.</span></span> <span data-ttu-id="ff6b7-109">Как и во многих объектах ADO, в зависимости от функциональных возможностей поставщика, некоторые коллекции **командных** объектов, методы или свойства могут создавать ошибки при указании ссылок.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-109">As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="ff6b7-110">Не всегда нужно создавать объект **Command** для выполнения команды в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-110">It is not always necessary to create a **Command** object to execute a command against a data source.</span></span> <span data-ttu-id="ff6b7-111">Можно использовать метод **EXECUTE** объекта **Connection** или метод **Open** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ff6b7-111">You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object.</span></span> <span data-ttu-id="ff6b7-112">Тем не менее, следует использовать объект **Command** , если необходимо повторно использовать команду в коде, или если вам нужно передать подробные сведения о параметрах с помощью команды.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-112">However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command.</span></span> <span data-ttu-id="ff6b7-113">Эти сценарии подробно описаны далее в этой главе.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-113">These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="ff6b7-114">Некоторые команды могут возвращать результирующий набор в виде двоичного потока или в виде одной записи, а не в качестве объекта Recordset, если он поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="ff6b7-115">Кроме того, некоторые команды не позволяют возвратить ни один набор результатов (например, запрос на обновление SQL).</span><span class="sxs-lookup"><span data-stu-id="ff6b7-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="ff6b7-116">В этой главе приводится наиболее типичный сценарий, но: выполнение команд, возвращающих результаты, в объект Recordset.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="ff6b7-117">Дополнительные сведения о возврате результатов в записи или потоки содержатся в [главе 10: записи и потоки](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="ff6b7-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="ff6b7-118">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="ff6b7-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="ff6b7-119">Обзор COM-объекта</span><span class="sxs-lookup"><span data-stu-id="ff6b7-119">Command object overview</span></span>](command-object-overview.md)
- [<span data-ttu-id="ff6b7-120">Создание и выполнение простой команды</span><span class="sxs-lookup"><span data-stu-id="ff6b7-120">Creating and executing a simple command</span></span>](creating-and-executing-a-simple-command.md)
- [<span data-ttu-id="ff6b7-121">Параметры COM-объекта</span><span class="sxs-lookup"><span data-stu-id="ff6b7-121">Command object parameters</span></span>](command-object-parameters.md)
- [<span data-ttu-id="ff6b7-122">Вызов хранимой процедуры с помощью команды</span><span class="sxs-lookup"><span data-stu-id="ff6b7-122">Calling a stored procedure with a command</span></span>](calling-a-stored-procedure-with-a-command.md)
- [<span data-ttu-id="ff6b7-123">Именованные команды</span><span class="sxs-lookup"><span data-stu-id="ff6b7-123">Named commands</span></span>](named-commands.md)
