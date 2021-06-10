---
title: Создание подключения
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 487212acd8847928e1fab405593edb172d0172d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289786"
---
# <a name="making-a-connection"></a><span data-ttu-id="d2167-102">Создание подключения</span><span class="sxs-lookup"><span data-stu-id="d2167-102">Making a connection</span></span>

<span data-ttu-id="d2167-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2167-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2167-104">Чтобы подключиться к источнику данных, необходимо указать строку *подключения,* параметры которой могут отличаться для каждого поставщика и источника данных.</span><span class="sxs-lookup"><span data-stu-id="d2167-104">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source.</span></span> <span data-ttu-id="d2167-105">Дополнительные сведения см. в [строке Создание строки подключения.](creating-the-connection-string.md)</span><span class="sxs-lookup"><span data-stu-id="d2167-105">For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="d2167-106">Чаще всего ADO открывает подключение с помощью метода **Open** объекта **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="d2167-106">ADO most commonly opens a connection by using the **Connection** object **Open** method.</span></span> <span data-ttu-id="d2167-107">Синтаксис метода **Open** показан здесь:</span><span class="sxs-lookup"><span data-stu-id="d2167-107">The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="d2167-108">Кроме того, вы можете вызвать метод ярлыка **Recordset.Open,** чтобы открыть неявное подключение и выдать команду над этим подключением в одной операции.</span><span class="sxs-lookup"><span data-stu-id="d2167-108">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation.</span></span> <span data-ttu-id="d2167-109">Сделайте это, передав допустимую строку подключения в качестве аргумента *ActiveConnection* **методу Open.**</span><span class="sxs-lookup"><span data-stu-id="d2167-109">Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method.</span></span> <span data-ttu-id="d2167-110">Вот синтаксис для каждого метода в Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d2167-110">Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="d2167-111">Когда следует использовать объект **Подключения** против **ярлыка Recordset.Open?**</span><span class="sxs-lookup"><span data-stu-id="d2167-111">When should you use a **Connection** object vs. the **Recordset.Open** shortcut?</span></span> <span data-ttu-id="d2167-112">Используйте объект **Подключение,** если планируется открыть несколько **наборов записей** или при выполнении нескольких команд.</span><span class="sxs-lookup"><span data-stu-id="d2167-112">Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands.</span></span> <span data-ttu-id="d2167-113">Подключение по-прежнему создается ADO неявно при использовании **ярлыка Recordset.Open.**</span><span class="sxs-lookup"><span data-stu-id="d2167-113">A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


