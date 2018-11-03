---
title: Подключения
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0335c4bbc0d1240d6d4ca53ceacf47bf44fce67d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945889"
---
# <a name="making-a-connection"></a><span data-ttu-id="ae244-102">Подключения</span><span class="sxs-lookup"><span data-stu-id="ae244-102">Making a connection</span></span>

<span data-ttu-id="ae244-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae244-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae244-104">Для подключения к источнику данных, необходимо указать *строку подключения*, параметры которого может отличаться для каждого поставщика и источника данных.</span><span class="sxs-lookup"><span data-stu-id="ae244-104">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source.</span></span> <span data-ttu-id="ae244-105">[Строка подключения](creating-the-connection-string.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="ae244-105">For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="ae244-106">Чаще всего ADO открывает подключение с помощью метода **Open** объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="ae244-106">ADO most commonly opens a connection by using the **Connection** object **Open** method.</span></span> <span data-ttu-id="ae244-107">Синтаксис метода **Open** показано ниже:</span><span class="sxs-lookup"><span data-stu-id="ae244-107">The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="ae244-108">Кроме того можно вызвать метод ярлык, **Recordset.Open**, для открытия неявные соединения и команды через это подключение за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="ae244-108">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation.</span></span> <span data-ttu-id="ae244-109">Это сделать, передав в качестве аргумента *ActiveConnection* метода **Open** в это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="ae244-109">Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method.</span></span> <span data-ttu-id="ae244-110">Ниже приведен синтаксис для каждого метода в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ae244-110">Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="ae244-111">Когда следует использовать объект **подключения** и ярлык **Recordset.Open** ?</span><span class="sxs-lookup"><span data-stu-id="ae244-111">When should you use a **Connection** object vs. the **Recordset.Open** shortcut?</span></span> <span data-ttu-id="ae244-112">Используйте объект **подключения** , если планируется открыть более одного **набора записей**или при выполнении нескольких команд.</span><span class="sxs-lookup"><span data-stu-id="ae244-112">Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands.</span></span> <span data-ttu-id="ae244-113">Подключение по-прежнему создается путем ADO неявно при использовании сочетания **Recordset.Open** .</span><span class="sxs-lookup"><span data-stu-id="ae244-113">A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


