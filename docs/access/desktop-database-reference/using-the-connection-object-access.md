---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480967"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="2f275-102">Using the Connection Object (Access)</span><span class="sxs-lookup"><span data-stu-id="2f275-102">Using the Connection Object (Access)</span></span>


<span data-ttu-id="2f275-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f275-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f275-104">Объект **подключения** представляет собой уникальный сеанс с источником данных.</span><span class="sxs-lookup"><span data-stu-id="2f275-104">A **Connection** object represents a unique session with a data source.</span></span> <span data-ttu-id="2f275-105">В случае с системой базы данных клиент сервер может быть лежат действительное сетевое подключение к серверу.</span><span class="sxs-lookup"><span data-stu-id="2f275-105">In the case of a client/server database system, it can be equivalent to an actual network connection to the server.</span></span> <span data-ttu-id="2f275-106">В зависимости от функциональных возможностей, поддерживаемых поставщика, некоторые семейств сайтов, методов или свойств **подключения** объекта могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="2f275-106">Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="2f275-107">Перед открытием объекта **подключения** необходимо определить определенную информацию о источник данных и тип подключения.</span><span class="sxs-lookup"><span data-stu-id="2f275-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="2f275-108">Параметр *ConnectionString* объекта **подключения к** методу **Open** , или свойство **ConnectionString** в объект **подключения** — обычно содержит большую часть информации.</span><span class="sxs-lookup"><span data-stu-id="2f275-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="2f275-109">Строка подключения — это строка символов, определяющий с переменным количеством аргументов.</span><span class="sxs-lookup"><span data-stu-id="2f275-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="2f275-110">Аргументы — некоторые необходимые для ADO, но другие пользователи поставщика — содержат сведения, которые должны иметь объект **подключения** к выполнять свою работу.</span><span class="sxs-lookup"><span data-stu-id="2f275-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="2f275-111">Аргументы, которые составляют параметр *ConnectionString* разделяются точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="2f275-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>


> [!NOTE]
> <P><span data-ttu-id="2f275-112">Также можно указать имя источника ODBC данных (DSN) или файла Data Link (UDL) в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="2f275-112">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</span></span> <span data-ttu-id="2f275-113">Дополнительные сведения о уведомления о доставке можно источников данных в части 1 <EM>Справочник программиста по ODBC</EM>.</span><span class="sxs-lookup"><span data-stu-id="2f275-113">For more information about DSNs, see Data Sources in Part 1 of the <EM>ODBC Programmer's Reference</EM>.</span></span> <span data-ttu-id="2f275-114">Дополнительные сведения о UDL см данных ссылок API в <EM>Справочник программиста OLE DB</EM>.</span><span class="sxs-lookup"><span data-stu-id="2f275-114">For more information about UDLs, see Data Link API Overview in the <EM>OLE DB Programmer's Reference</EM>.</span></span></P>


