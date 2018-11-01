---
title: Подсчет строк (Справочник по для настольных баз данных Access)
TOCTitle: Counting Rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 664e7022d3a49f7c4c7c1fa6122b05a230b6e297
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889653"
---
# <a name="counting-rows"></a><span data-ttu-id="85032-102">Подсчет строк</span><span class="sxs-lookup"><span data-stu-id="85032-102">Counting Rows</span></span>


<span data-ttu-id="85032-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85032-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85032-104">Свойство **RecordCount** возвращает значение типа **Long** , показывает, сколько записей в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="85032-104">The **RecordCount** property returns a **Long** value that indicates the number of records in the **Recordset**.</span></span> <span data-ttu-id="85032-105">Используйте свойство **RecordCount** , чтобы узнать, сколько записей, в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="85032-105">Use the **RecordCount** property to find out how many records are in a **Recordset** object.</span></span> <span data-ttu-id="85032-106">Это свойство возвращает значение -1 при ADO не может определить число записей, или если поставщик или тип курсора не поддерживает **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="85032-106">The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**.</span></span> <span data-ttu-id="85032-107">Чтение свойства **RecordCount** на закрытой **набора записей** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="85032-107">Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="85032-108">Свойство **RecordCount** зависит от возможностей поставщика и тип курсора.</span><span class="sxs-lookup"><span data-stu-id="85032-108">The **RecordCount** property depends on the capabilities of the provider and the type of cursor.</span></span> <span data-ttu-id="85032-109">Свойство **RecordCount** возвращает значение -1 для последовательный курсор, фактическое количество для статического или курсор набора ключей, а также значение -1 или фактический количество для динамического курсора, в зависимости от источника данных.</span><span class="sxs-lookup"><span data-stu-id="85032-109">The **RecordCount** property will return -1 for a forward-only cursor, the actual count for a static or keyset cursor, and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

<span data-ttu-id="85032-110">Пример **набора записей** , введенные в [Анализ данных](chapter-3-examining-data.md) возвратит – 1, так как последовательный курсор был открыт.</span><span class="sxs-lookup"><span data-stu-id="85032-110">The sample **Recordset** introduced in [Examining Data](chapter-3-examining-data.md) would return –1 because a forward-only cursor was opened.</span></span> <span data-ttu-id="85032-111">Чтобы использовать свойство **RecordCount** , необходимо открыть **набора записей** с помощью более сложных текущей позиции (static или набора ключей).</span><span class="sxs-lookup"><span data-stu-id="85032-111">In order to use the **RecordCount** property, you would need to open the **Recordset** with a more sophisticated cursor (static or keyset).</span></span>

<span data-ttu-id="85032-112">В некоторых случаях поставщик или текущей позиции смогут для предоставления значения **RecordCount** без получения все записи из источника данных.</span><span class="sxs-lookup"><span data-stu-id="85032-112">In certain cases, your provider or cursor might be unable to provide the **RecordCount** value without first fetching all records from the data source.</span></span> <span data-ttu-id="85032-113">Чтобы принудительно этот тип выборки, вызовите метод **MoveLast** **записей** до вызова метода **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="85032-113">To force this type of fetch, call the **Recordset** **MoveLast** method before calling **RecordCount**.</span></span>

<span data-ttu-id="85032-114">При необходимости замените строку кода, вызывающего метод **Open** **записей** со следующими:</span><span class="sxs-lookup"><span data-stu-id="85032-114">If you were to replace the line of code that calls the **Recordset** **Open** method with the following:</span></span>

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="85032-115">Используйте свойство **RecordCount** , так как статические курсоры с [Поставщик Microsoft OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md) поддерживает **RecordCount**смогут.</span><span class="sxs-lookup"><span data-stu-id="85032-115">you would be able to use the **RecordCount** property because static cursors with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) support **RecordCount**.</span></span> <span data-ttu-id="85032-116">Например следующий код будет распечатать число записей, возвращаемых с помощью команды в окно отладки, если предположить, что курсор поддерживает свойство **RecordCount** :</span><span class="sxs-lookup"><span data-stu-id="85032-116">For example, the following code would print out the number of records returned by the command to the debug window, assuming the cursor supports the **RecordCount** property:</span></span>

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

<span data-ttu-id="85032-117">С этого момента предполагается, что эти более производительные (но более дорогое) курсор и блокировки типа используются параметры.</span><span class="sxs-lookup"><span data-stu-id="85032-117">From this point forward, assume that these more capable (but more expensive) cursor and lock type settings are used.</span></span>

