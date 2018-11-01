---
title: Дополнительные сведения о сохранения наборов записей
TOCTitle: More About Recordset Persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: baf1e4976b9669deed0a80f6405127afc88d521e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878295"
---
# <a name="more-about-recordset-persistence"></a><span data-ttu-id="29fab-102">Дополнительные сведения о сохранения наборов записей</span><span class="sxs-lookup"><span data-stu-id="29fab-102">More About Recordset Persistence</span></span>


<span data-ttu-id="29fab-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29fab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29fab-104">Объект ADO Recordset поддерживает хранение содержимого объекта **набора записей** в файл с помощью метода [сохранения](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="29fab-104">The ADO Recordset object supports storing a **Recordset** object's contents in a file using its [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="29fab-105">Постоянно хранимых файл существует на локальном диске, сетевом сервере или как URL-адрес веб-сайту.</span><span class="sxs-lookup"><span data-stu-id="29fab-105">The persistently stored file may exist on a local drive, network server, or as a URL on a website.</span></span> <span data-ttu-id="29fab-106">Более поздних версий файл можно восстановить с помощью любого из объекта **набора** [Open](open-method-ado-recordset.md) метод или метод [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="29fab-106">Later, the file can be restored with either the **Recordset** object's [Open](open-method-ado-recordset.md) method or the [Connection](connection-object-ado.md) object's [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method.</span></span>

<span data-ttu-id="29fab-107">Кроме того метод [GetString](getstring-method-ado.md) преобразует объект **набора записей** в форму, в которой столбцы и строки разделяются знаков.</span><span class="sxs-lookup"><span data-stu-id="29fab-107">In addition, the [GetString](getstring-method-ado.md) method converts a **Recordset** object to a form in which the columns and rows are delimited with characters you specify.</span></span>

<span data-ttu-id="29fab-108">Для сохранения **записей**, начните с преобразование в форме, которые могут храниться в файле.</span><span class="sxs-lookup"><span data-stu-id="29fab-108">To persist a **Recordset**, begin by converting it to a form that can be stored in a file.</span></span> <span data-ttu-id="29fab-109">Объекты **набора записей** могут храниться в собственный формат расширенного данных TableGram (ADTG) или форматов open языке (XML).</span><span class="sxs-lookup"><span data-stu-id="29fab-109">**Recordset** objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format.</span></span> <span data-ttu-id="29fab-110">Ниже приводятся примеры ADTG.</span><span class="sxs-lookup"><span data-stu-id="29fab-110">ADTG examples are shown below.</span></span> <span data-ttu-id="29fab-111">Дополнительные сведения о хранение в XML можно [Сохранение записей в формате XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="29fab-111">For more information about XML persistence, see [Persisting Records in XML format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="29fab-112">Сохраните все ожидающие изменения в файле постоянных.</span><span class="sxs-lookup"><span data-stu-id="29fab-112">Save any pending changes in the persisted file.</span></span> <span data-ttu-id="29fab-113">Это позволяет выдавать запрос, возвращающий объект **набора записей** редактирует **записей**, сохраняет его и ожидающие изменения, позднее восстанавливает **набора записей**и затем обновляет источник данных с помощью сохраненных ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="29fab-113">Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.</span></span>

<span data-ttu-id="29fab-114">Сведения о постоянно хранение объектов **потока** содержатся в разделе [потоки и сохраняемость](streams-and-persistence.md) Глава 10.</span><span class="sxs-lookup"><span data-stu-id="29fab-114">For information about persistently storing **Stream** objects, see [Streams and Persistence](streams-and-persistence.md) in Chapter 10.</span></span>

<span data-ttu-id="29fab-115">Пример сохранения **записей** содержатся в [Сценарий хранение записей XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="29fab-115">For an example of **Recordset** persistence, see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

## <a name="example"></a><span data-ttu-id="29fab-116">Пример</span><span class="sxs-lookup"><span data-stu-id="29fab-116">Example</span></span>

<span data-ttu-id="29fab-117">**Сохранение набора записей:**</span><span class="sxs-lookup"><span data-stu-id="29fab-117">**Save a Recordset:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

<span data-ttu-id="29fab-118">**Откройте сохраненный файл с Recordset.Open:**</span><span class="sxs-lookup"><span data-stu-id="29fab-118">**Open a persisted file with Recordset.Open:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

<span data-ttu-id="29fab-119">При необходимости Если **записей** нет активного подключения, можно принять значения по умолчанию и просто кода ниже:</span><span class="sxs-lookup"><span data-stu-id="29fab-119">Optionally, if the **Recordset** does not have an active connection, you can accept all the defaults and simply code the following:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

<span data-ttu-id="29fab-120">**Откройте сохраненный файл с Connection.Execute:**</span><span class="sxs-lookup"><span data-stu-id="29fab-120">**Open a persisted file with Connection.Execute:**</span></span>

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

<span data-ttu-id="29fab-121">**Откройте сохраненный файл с RDS. DataControl:**</span><span class="sxs-lookup"><span data-stu-id="29fab-121">**Open a persisted file with RDS.DataControl:**</span></span>

<span data-ttu-id="29fab-122">В этом случае свойство **сервера** не задан.</span><span class="sxs-lookup"><span data-stu-id="29fab-122">In this case, the **Server** property is not set.</span></span>

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

