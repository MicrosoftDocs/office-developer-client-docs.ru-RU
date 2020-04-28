---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d16b802140e2dcbbd85988bee316ae27236c3235
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305924"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="f6d79-102">Использование объекта Connection (Access)</span><span class="sxs-lookup"><span data-stu-id="f6d79-102">Using the Connection object (Access)</span></span>


<span data-ttu-id="f6d79-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6d79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6d79-104">Объект **Connection** представляет уникальный сеанс с источником данных.</span><span class="sxs-lookup"><span data-stu-id="f6d79-104">A **Connection** object represents a unique session with a data source.</span></span> <span data-ttu-id="f6d79-105">В случае с клиент-серверной системой базы данных она может быть эквивалентна фактическому сетевому подключению к серверу.</span><span class="sxs-lookup"><span data-stu-id="f6d79-105">In the case of a client/server database system, it can be equivalent to an actual network connection to the server.</span></span> <span data-ttu-id="f6d79-106">В зависимости от функциональных возможностей, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Connection** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="f6d79-106">Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="f6d79-107">Перед открытием объекта **подключения** необходимо определить определенные сведения об источнике данных и типе подключения.</span><span class="sxs-lookup"><span data-stu-id="f6d79-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="f6d79-108">Параметр *ConnectionString* метода **Open** объекта **Connection** или свойство **ConnectionString** объекта **Connection** , как правило, содержит большую часть этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f6d79-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="f6d79-109">Строка подключения — это строка символов, определяющая переменное число аргументов.</span><span class="sxs-lookup"><span data-stu-id="f6d79-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="f6d79-110">Аргументы, некоторые из которых необходимы для ADO, а другие — для конкретных поставщиков, содержат сведения, необходимые объекту **Connection** для выполнения своей работы.</span><span class="sxs-lookup"><span data-stu-id="f6d79-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="f6d79-111">Аргументы, составляющие параметр *ConnectionString* , разделяются точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="f6d79-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="f6d79-112">Кроме того, можно указать имя источника данных ODBC (DSN) или файл канала данных (UDL) в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="f6d79-112">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</span></span> <span data-ttu-id="f6d79-113">Дополнительные сведения о DSN приведены в статье источники данных в части 1 *Справочника программиста ODBC*.</span><span class="sxs-lookup"><span data-stu-id="f6d79-113">For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*.</span></span> <span data-ttu-id="f6d79-114">Дополнительные сведения о Удлс можно найти в статье Обзор API каналов передачи данных в *справочнике программиста по OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="f6d79-114">For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="f6d79-115">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="f6d79-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="f6d79-116">Создание строки подключения</span><span class="sxs-lookup"><span data-stu-id="f6d79-116">Creating the connection string</span></span>](creating-the-connection-string.md)
- [<span data-ttu-id="f6d79-117">Управление транзакциями</span><span class="sxs-lookup"><span data-stu-id="f6d79-117">Controlling transactions</span></span>](controlling-transactions.md)
