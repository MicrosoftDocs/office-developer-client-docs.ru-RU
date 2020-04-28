---
title: Дополнительные сведения о сохранении наборов записей
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 194dcf3826409c91f8d046b39b9009b43aee5477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288850"
---
# <a name="more-about-recordset-persistence"></a><span data-ttu-id="d38b8-102">Дополнительные сведения о сохранении наборов записей</span><span class="sxs-lookup"><span data-stu-id="d38b8-102">More about Recordset persistence</span></span>

<span data-ttu-id="d38b8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d38b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d38b8-104">Объект ADO Recordset поддерживает сохранение содержимого объекта **Recordset** в файле с помощью метода [Save](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d38b8-104">The ADO Recordset object supports storing a **Recordset** object's contents in a file using its [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="d38b8-105">Сохраняемый файл может находиться на локальном диске, сетевом сервере или в виде URL-адреса на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="d38b8-105">The persistently stored file may exist on a local drive, network server, or as a URL on a website.</span></span> <span data-ttu-id="d38b8-106">Позже файл можно восстановить с помощью метода [Open](open-method-ado-recordset.md) объекта **Recordset** или метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d38b8-106">Later, the file can be restored with either the **Recordset** object's [Open](open-method-ado-recordset.md) method or the [Connection](connection-object-ado.md) object's [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method.</span></span>

<span data-ttu-id="d38b8-107">Кроме того, метод [GetString](getstring-method-ado.md) преобразует объект **Recordset** в форму, в которой столбцы и строки разделяются указанными символами.</span><span class="sxs-lookup"><span data-stu-id="d38b8-107">In addition, the [GetString](getstring-method-ado.md) method converts a **Recordset** object to a form in which the columns and rows are delimited with characters you specify.</span></span>

<span data-ttu-id="d38b8-108">Чтобы сохранить **набор записей**, начните с преобразования его в форму, которая может храниться в файле.</span><span class="sxs-lookup"><span data-stu-id="d38b8-108">To persist a **Recordset**, begin by converting it to a form that can be stored in a file.</span></span> <span data-ttu-id="d38b8-109">Объекты **Recordset** могут храниться в формате дополнительных данных ТАБЛЕГРАМ (адтг) или формате Open Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="d38b8-109">**Recordset** objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format.</span></span> <span data-ttu-id="d38b8-110">Примеры АДТГ приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="d38b8-110">ADTG examples are shown below.</span></span> <span data-ttu-id="d38b8-111">Для получения дополнительных сведений о сохраняемости [в формате](persisting-records-in-xml-format.md)XML см.</span><span class="sxs-lookup"><span data-stu-id="d38b8-111">For more information about XML persistence, see [Persisting Records in XML format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="d38b8-112">Сохраните все ожидающие изменения в материализованном файле.</span><span class="sxs-lookup"><span data-stu-id="d38b8-112">Save any pending changes in the persisted file.</span></span> <span data-ttu-id="d38b8-113">Это позволяет выдать запрос, возвращающий объект **Recordset** , изменяя **набор записей**, сохраняет его и ожидающие изменения **, в дальнейшем**восстанавливает источник данных с сохранением всех ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="d38b8-113">Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.</span></span>

<span data-ttu-id="d38b8-114">Сведения о постоянном хранении объектов **Stream** [можно найти в](streams-and-persistence.md) статье 10.</span><span class="sxs-lookup"><span data-stu-id="d38b8-114">For information about persistently storing **Stream** objects, see [Streams and Persistence](streams-and-persistence.md) in Chapter 10.</span></span>

<span data-ttu-id="d38b8-115">Пример сохраняемости в **наборе записей** представлен в [сценарии сохраняемости в XML Recordset](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="d38b8-115">For an example of **Recordset** persistence, see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

## <a name="example"></a><span data-ttu-id="d38b8-116">Пример</span><span class="sxs-lookup"><span data-stu-id="d38b8-116">Example</span></span>

<span data-ttu-id="d38b8-117">**Сохранение набора записей:**</span><span class="sxs-lookup"><span data-stu-id="d38b8-117">**Save a Recordset:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

<span data-ttu-id="d38b8-118">**Откройте постоянный файл с помощью объекта Recordset. Open:**</span><span class="sxs-lookup"><span data-stu-id="d38b8-118">**Open a persisted file with Recordset.Open:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

<span data-ttu-id="d38b8-119">При необходимости вы можете принять все значения по умолчанию, если в **наборе записей** нет активного подключения, и просто закодировать следующее:</span><span class="sxs-lookup"><span data-stu-id="d38b8-119">Optionally, if the **Recordset** does not have an active connection, you can accept all the defaults and simply code the following:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

<span data-ttu-id="d38b8-120">**Откройте постоянный файл с подключением. Execute:**</span><span class="sxs-lookup"><span data-stu-id="d38b8-120">**Open a persisted file with Connection.Execute:**</span></span>

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

<span data-ttu-id="d38b8-121">**Откройте постоянный файл с помощью RDS. DataControl**</span><span class="sxs-lookup"><span data-stu-id="d38b8-121">**Open a persisted file with RDS.DataControl:**</span></span>

<span data-ttu-id="d38b8-122">В этом случае свойство **Server** не задается.</span><span class="sxs-lookup"><span data-stu-id="d38b8-122">In this case, the **Server** property is not set.</span></span>

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

