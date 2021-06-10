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
# <a name="using-the-connection-object-access"></a><span data-ttu-id="27cc8-102">Использование объекта Подключения (Access)</span><span class="sxs-lookup"><span data-stu-id="27cc8-102">Using the Connection object (Access)</span></span>


<span data-ttu-id="27cc8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27cc8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27cc8-104">Объект **Connection** представляет собой уникальный сеанс с источником данных.</span><span class="sxs-lookup"><span data-stu-id="27cc8-104">A **Connection** object represents a unique session with a data source.</span></span> <span data-ttu-id="27cc8-105">В случае системы базы данных клиента и сервера она может быть эквивалентна фактическому сетевому подключению к серверу.</span><span class="sxs-lookup"><span data-stu-id="27cc8-105">In the case of a client/server database system, it can be equivalent to an actual network connection to the server.</span></span> <span data-ttu-id="27cc8-106">В зависимости от функций, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Подключения** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="27cc8-106">Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="27cc8-107">Перед открытием **объекта Подключения** необходимо определить определенные сведения о источнике данных и типе подключения.</span><span class="sxs-lookup"><span data-stu-id="27cc8-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="27cc8-108">Параметр *ConnectionString* метода Open  объекта **Подключения** или свойства **ConnectionString** на объекте **Подключение** обычно содержит большую часть этой информации.</span><span class="sxs-lookup"><span data-stu-id="27cc8-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="27cc8-109">Строка подключения — это строка символов, определяемая переменным числом аргументов.</span><span class="sxs-lookup"><span data-stu-id="27cc8-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="27cc8-110">Аргументы , некоторые из которых требуются ADO, но другие — для конкретного поставщика, содержат сведения о том, что объект **Connection** должен выполнять свою работу.</span><span class="sxs-lookup"><span data-stu-id="27cc8-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="27cc8-111">Аргументы, которые составляют параметр *ConnectionString,* разделены с ;).</span><span class="sxs-lookup"><span data-stu-id="27cc8-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="27cc8-112">Вы также можете указать имя источника данных ODBC (DSN) или файл ссылки данных (UDL) в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="27cc8-112">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</span></span> <span data-ttu-id="27cc8-113">Дополнительные сведения о DSNs см. в части 1 ссылки программиста *ODBC.*</span><span class="sxs-lookup"><span data-stu-id="27cc8-113">For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*.</span></span> <span data-ttu-id="27cc8-114">Дополнительные сведения о UDLs см. в обзоре API ссылки на данные в справке программиста *OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="27cc8-114">For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="27cc8-115">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="27cc8-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="27cc8-116">Создание строки подключения</span><span class="sxs-lookup"><span data-stu-id="27cc8-116">Creating the connection string</span></span>](creating-the-connection-string.md)
- [<span data-ttu-id="27cc8-117">Управление транзакциями</span><span class="sxs-lookup"><span data-stu-id="27cc8-117">Controlling transactions</span></span>](controlling-transactions.md)
