---
title: Этап 2. Вызов серверной программы (руководство по RDS)
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d3264c58434bf7af6ae4e75c249a7009f39b7d4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947233"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a><span data-ttu-id="f6a59-102">Шаг 2: Вызова программы сервера (учебник служб удаленных рабочих СТОЛОВ)</span><span class="sxs-lookup"><span data-stu-id="f6a59-102">Step 2: Invoke the server program (RDS Tutorial)</span></span>

<span data-ttu-id="f6a59-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6a59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6a59-104">При вызове метода для клиента *прокси-сервера*, самой программы на сервере выполняется метод.</span><span class="sxs-lookup"><span data-stu-id="f6a59-104">When you invoke a method on the client *proxy*, the actual program on the server executes the method.</span></span> <span data-ttu-id="f6a59-105">На этом этапе будет выполнить запрос на сервере.</span><span class="sxs-lookup"><span data-stu-id="f6a59-105">In this step, you'll execute a query on the server.</span></span>

<span data-ttu-id="f6a59-106">**Часть "A"** Если не были [RDSServer.DataFactory](datafactory-object-rdsserver.md) в этом руководстве, самый удобный способ выполните этот шаг будет использовать [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="f6a59-106">**Part A**If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="f6a59-107">**RDS. DataControl** объединяет предыдущие действия по созданию прокси-сервер, с помощью этот шаг, выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="f6a59-107">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

<span data-ttu-id="f6a59-108">Установка **RDS. DataControl** объекта свойства [сервера](server-property-rds.md) для идентификации, где следует присвоить значение программы сервера; свойства [подключения](connect-property-rds.md) , чтобы указать строки подключения для доступа к источнику данных; и свойства [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) , чтобы указать текст команды запроса.</span><span class="sxs-lookup"><span data-stu-id="f6a59-108">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated; the [Connect](connect-property-rds.md) property to specify the connect string to access the data source; and the [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) property to specify the query command text.</span></span> <span data-ttu-id="f6a59-109">Затем заключать метод [Refresh](refresh-method-rds.md) , чтобы программа server для подключения к источнику данных, извлечение строк, указанным в запросе и возвращают объект **набора записей** клиенту.</span><span class="sxs-lookup"><span data-stu-id="f6a59-109">Then issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="f6a59-110">В этом руководстве не использует **RDS. DataControl**, но это, как она будет выглядеть при как:</span><span class="sxs-lookup"><span data-stu-id="f6a59-110">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<span data-ttu-id="f6a59-111">Ни учебника по вызов служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:</span><span class="sxs-lookup"><span data-stu-id="f6a59-111">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

<span data-ttu-id="f6a59-112">**Часть "B"** Общий метод выполнения этого этапа — это для вызова метода [Query](query-method-rds.md) объекта **RDSServer.DataFactory** .</span><span class="sxs-lookup"><span data-stu-id="f6a59-112">**Part B**The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="f6a59-113">Этот метод принимает строку подключения, которая используется для подключения к источнику данных, и текст команды, который используется для указания строк, возвращаемых из источника данных.</span><span class="sxs-lookup"><span data-stu-id="f6a59-113">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="f6a59-114">В этом руководстве использует объект **DataFactory** метод **запроса** :</span><span class="sxs-lookup"><span data-stu-id="f6a59-114">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

