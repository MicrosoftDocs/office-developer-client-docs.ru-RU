---
title: Подсчет строк (справочник по базе данных Access для настольных ПК)
TOCTitle: Counting rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2388978185ac29149f7f15150ccfdbc559cc910f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295417"
---
# <a name="counting-rows"></a><span data-ttu-id="b58a0-102">Подсчет строк</span><span class="sxs-lookup"><span data-stu-id="b58a0-102">Counting rows</span></span>


<span data-ttu-id="b58a0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b58a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b58a0-104">Свойство **RecordCount** возвращает  длинное значение, которое указывает количество записей в **наборе recordset.**</span><span class="sxs-lookup"><span data-stu-id="b58a0-104">The **RecordCount** property returns a **Long** value that indicates the number of records in the **Recordset**.</span></span> <span data-ttu-id="b58a0-105">Используйте свойство **RecordCount,** чтобы узнать, сколько записей находится в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b58a0-105">Use the **RecordCount** property to find out how many records are in a **Recordset** object.</span></span> <span data-ttu-id="b58a0-106">Свойство возвращает -1, если ADO не может определить количество записей или если поставщик или тип курсора не поддерживает **RecordCount.**</span><span class="sxs-lookup"><span data-stu-id="b58a0-106">The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**.</span></span> <span data-ttu-id="b58a0-107">Чтение свойства **RecordCount** в закрытом наборе **записей** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b58a0-107">Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="b58a0-108">Свойство **RecordCount** зависит от возможностей поставщика и типа курсора.</span><span class="sxs-lookup"><span data-stu-id="b58a0-108">The **RecordCount** property depends on the capabilities of the provider and the type of cursor.</span></span> <span data-ttu-id="b58a0-109">Свойство **RecordCount** возвращает -1 для курсора только вперед, фактическое число для статического или ключевого курсора, а также -1 или фактическое число динамического курсора в зависимости от источника данных.</span><span class="sxs-lookup"><span data-stu-id="b58a0-109">The **RecordCount** property will return -1 for a forward-only cursor, the actual count for a static or keyset cursor, and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

<span data-ttu-id="b58a0-110">Пример **recordset,** введенный в [анализе данных,](chapter-3-examining-data.md) возвратит –1, так как был открыт курсор "только вперед".</span><span class="sxs-lookup"><span data-stu-id="b58a0-110">The sample **Recordset** introduced in [Examining Data](chapter-3-examining-data.md) would return –1 because a forward-only cursor was opened.</span></span> <span data-ttu-id="b58a0-111">Чтобы использовать свойство **RecordCount,** необходимо открыть объект **Recordset** с более сложным курсором (статическим или набором клавиш).</span><span class="sxs-lookup"><span data-stu-id="b58a0-111">In order to use the **RecordCount** property, you would need to open the **Recordset** with a more sophisticated cursor (static or keyset).</span></span>

<span data-ttu-id="b58a0-112">В некоторых случаях поставщик или курсор не смогут предоставить значение **RecordCount,** не извлекая все записи из источника данных.</span><span class="sxs-lookup"><span data-stu-id="b58a0-112">In certain cases, your provider or cursor might be unable to provide the **RecordCount** value without first fetching all records from the data source.</span></span> <span data-ttu-id="b58a0-113">Чтобы принудительно получить этот тип, вызовите метод **Recordset** **MoveLast** перед вызовом **RecordCount.**</span><span class="sxs-lookup"><span data-stu-id="b58a0-113">To force this type of fetch, call the **Recordset** **MoveLast** method before calling **RecordCount**.</span></span>

<span data-ttu-id="b58a0-114">Если необходимо заменить строку кода, которая вызывает метод **Recordset** **Open,** следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="b58a0-114">If you were to replace the line of code that calls the **Recordset** **Open** method with the following:</span></span>

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="b58a0-115">вы сможете использовать свойство **RecordCount,** так как статические курсоры с поставщиком [Microsoft OLE DB для](microsoft-ole-db-provider-for-sql-server.md) SQL Server **recordCount.**</span><span class="sxs-lookup"><span data-stu-id="b58a0-115">you would be able to use the **RecordCount** property because static cursors with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) support **RecordCount**.</span></span> <span data-ttu-id="b58a0-116">Например, следующий код выпечатает количество записей, возвращенных командой, в окне отлажений при условии, что курсор поддерживает свойство **RecordCount:**</span><span class="sxs-lookup"><span data-stu-id="b58a0-116">For example, the following code would print out the number of records returned by the command to the debug window, assuming the cursor supports the **RecordCount** property:</span></span>

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

<span data-ttu-id="b58a0-117">С этого момента предположим, что используются эти более способные (но более затратные) параметры курсора и типа блокировки.</span><span class="sxs-lookup"><span data-stu-id="b58a0-117">From this point forward, assume that these more capable (but more expensive) cursor and lock type settings are used.</span></span>

