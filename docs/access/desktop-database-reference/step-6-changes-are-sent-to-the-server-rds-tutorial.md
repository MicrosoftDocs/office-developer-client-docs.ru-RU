---
title: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d26ca621ba7102dc0f9c6219ba3a16b28138770f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481246"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a><span data-ttu-id="8be1b-102">Step 6: Changes are Sent to the Server (RDS Tutorial)</span><span class="sxs-lookup"><span data-stu-id="8be1b-102">Step 6: Changes are Sent to the Server (RDS Tutorial)</span></span>


<span data-ttu-id="8be1b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8be1b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8be1b-104">При редактировании объекта **набора записей** (строк, которые будут добавлены, изменены или удалены) изменения можно отправить на сервер.</span><span class="sxs-lookup"><span data-stu-id="8be1b-104">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8be1b-105">Поведение по умолчанию служб удаленных рабочих СТОЛОВ можно вызвать неявно с объекты ADO и поставщик удаленного взаимодействия Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8be1b-105">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="8be1b-106">Запросы могут возвращать s <STRONG>записей</STRONG>и измененного s <STRONG>записей</STRONG>можно обновить источник данных.</span><span class="sxs-lookup"><span data-stu-id="8be1b-106">Queries can return <STRONG>Recordset</STRONG>s, and edited <STRONG>Recordset</STRONG>s can update the data source.</span></span> <span data-ttu-id="8be1b-107">В этом руководстве не вызывает служб удаленных рабочих СТОЛОВ с объектами ADO, но это, как она будет выглядеть при как:</span><span class="sxs-lookup"><span data-stu-id="8be1b-107">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span></P>



```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

<span data-ttu-id="8be1b-108">**Часть "A"**</span><span class="sxs-lookup"><span data-stu-id="8be1b-108">**Part A**</span></span> 

<span data-ttu-id="8be1b-109">Предположим, в этом случае только использовали [RDS. DataControl](datacontrol-object-rds.md) , а теперь — объект **набора записей** , связанных с **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="8be1b-109">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="8be1b-110">Метод [SubmitChanges](submitchanges-method-rds.md) обновляет источник данных все изменения в объект **набора записей** Если свойства [сервера](server-property-rds.md) и [подключение](connect-property-rds.md) по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="8be1b-110">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

<span data-ttu-id="8be1b-111">**Часть "B"**</span><span class="sxs-lookup"><span data-stu-id="8be1b-111">**Part B**</span></span> 

<span data-ttu-id="8be1b-112">Кроме того может обновить сервер с объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) определения подключения и объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8be1b-112">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```

<span data-ttu-id="8be1b-113">**Это конце обучения.**</span><span class="sxs-lookup"><span data-stu-id="8be1b-113">**This is the end of the tutorial.**</span></span>

