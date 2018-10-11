---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480232"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="81efa-102">Using the Command Object (Access)</span><span class="sxs-lookup"><span data-stu-id="81efa-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="81efa-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="81efa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="81efa-104">После подключения к источнику данных, необходимые для выполнения запросов к нему для получения наборы результатов.</span><span class="sxs-lookup"><span data-stu-id="81efa-104">After connecting to a data source, you need to execute requests against it to obtain result sets.</span></span> <span data-ttu-id="81efa-105">ADO инкапсулирует этот тип функции команды в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="81efa-105">ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="81efa-106">Чтобы запросить любой тип операции у поставщика, при условии, что поставщик воспринимает строки команды должным образом, можно использовать объект **команды** .</span><span class="sxs-lookup"><span data-stu-id="81efa-106">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly.</span></span> <span data-ttu-id="81efa-107">Стандартная операция для поставщиков данных — для запросов к базе данных и возврата записей в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="81efa-107">A common operation for data providers is to query a database and return records in a **Recordset** object.</span></span> <span data-ttu-id="81efa-108">S **записей**будет описан далее в это, а также другие разделы; что их как наборы средств для хранения и просмотра результатов.</span><span class="sxs-lookup"><span data-stu-id="81efa-108">**Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets.</span></span> <span data-ttu-id="81efa-109">С помощью многие объекты ADO, в зависимости от функциональности поставщика, некоторые **команды** коллекций объектов, методов или свойств могут возникнуть ошибки при обращении к.</span><span class="sxs-lookup"><span data-stu-id="81efa-109">As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="81efa-110">Не всегда необходимо создать объект **команды** для выполнения команды в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="81efa-110">It is not always necessary to create a **Command** object to execute a command against a data source.</span></span> <span data-ttu-id="81efa-111">Метод **Execute** объекта **подключения** или метод **Open** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="81efa-111">You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object.</span></span> <span data-ttu-id="81efa-112">Тем не менее если вам потребуется повторно использовать команды в коде, или если нужно передать параметр detailed сведения с вашего команды следует использовать объект **команды** .</span><span class="sxs-lookup"><span data-stu-id="81efa-112">However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command.</span></span> <span data-ttu-id="81efa-113">Более подробно далее в этой главе рассматриваются следующие сценарии.</span><span class="sxs-lookup"><span data-stu-id="81efa-113">These scenarios are covered in more detail later in this chapter.</span></span>


> [!NOTE]
> <P><span data-ttu-id="81efa-114">Некоторые <STRONG>команды</STRONG>s может вернуть результирующего набора в виде двоичного потока или как одной <STRONG>записи</STRONG> , а не как <STRONG>набора записей</STRONG>, если это поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="81efa-114">Certain <STRONG>Command</STRONG>s can return a result set as a binary stream or as a single <STRONG>Record</STRONG> rather than as a <STRONG>Recordset</STRONG>, if this is supported by the provider.</span></span> <span data-ttu-id="81efa-115">Кроме того некоторые <STRONG>команды</STRONG>s не предназначены для вернуть любой вообще (например, обновление SQL запроса).</span><span class="sxs-lookup"><span data-stu-id="81efa-115">Also, some <STRONG>Command</STRONG>s are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="81efa-116">В этой главе будут рассмотрены наиболее типичные сценарии, однако: выполнение <STRONG>команды</STRONG>s, возвращать результаты в объект <STRONG>набора записей</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="81efa-116">This chapter will cover the most typical scenario, however: executing <STRONG>Command</STRONG>s that return results into a <STRONG>Recordset</STRONG> object.</span></span> <span data-ttu-id="81efa-117">Дополнительные сведения о возврате результатов в <STRONG>записи</STRONG>или <STRONG>потока</STRONG>можно <A href="chapter-10-records-and-streams.md">Глава 10: записей и потоков</A>.</span><span class="sxs-lookup"><span data-stu-id="81efa-117">For more information about returning results into <STRONG>Record</STRONG>s or <STRONG>Stream</STRONG>s, see <A href="chapter-10-records-and-streams.md">Chapter 10: Records and Streams</A>.</span></span></P>


