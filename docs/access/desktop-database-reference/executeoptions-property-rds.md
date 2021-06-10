---
title: Свойство ExecuteOptions (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf773090ccb37bf4cad4aff41499ad01f966479
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293254"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="a089d-102">Свойство ExecuteOptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="a089d-102">ExecuteOptions property (RDS)</span></span>


<span data-ttu-id="a089d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a089d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a089d-104">Указывает, включено ли асинхронное выполнение.</span><span class="sxs-lookup"><span data-stu-id="a089d-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a089d-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="a089d-105">Settings and return values</span></span>

<span data-ttu-id="a089d-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a089d-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a089d-107">Константа</span><span class="sxs-lookup"><span data-stu-id="a089d-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="a089d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a089d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a089d-109"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="a089d-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="a089d-110">Выполняет следующее синхронное обновление <a href="recordset-object-ado.md">Recordset.</a></span><span class="sxs-lookup"><span data-stu-id="a089d-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a089d-111"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="a089d-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="a089d-112">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a089d-112">Default.</span></span> <span data-ttu-id="a089d-113">Выполняет следующее обновление асинхронно <strong>recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="a089d-113">Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a089d-114">Каждый исполняемый клиентский файл, использующий эти константы, должен предоставлять для них объявления.</span><span class="sxs-lookup"><span data-stu-id="a089d-114">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="a089d-115">Вы можете вырезать и ввести постоянные объявления, которые нужны из файла Adcvbs.inc, расположенного в папке C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="a089d-115">You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="a089d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a089d-116">Remarks</span></span>

<span data-ttu-id="a089d-117">Если **в executeOptions** задан **adcExecAsync,** то это асинхронно выполняет следующий вызов **обновления** в [RDS. Набор](datacontrol-object-rds.md) записей объекта DataControl.</span><span class="sxs-lookup"><span data-stu-id="a089d-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="a089d-118">Если вы попробуете вызвать [сброс,](reset-method-rds.md) [обновить,](refresh-method-rds.md) [отправитьChanges,](submitchanges-method-rds.md) [CancelUpdate](cancelupdate-method-ado.md)или [Recordset,](recordset-sourcerecordset-properties-rds.md) а также другую асинхронную операцию, которая может изменить [RDS. Выполняется набор](datacontrol-object-rds.md) записей объекта DataControl, возникает ошибка. </span><span class="sxs-lookup"><span data-stu-id="a089d-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="a089d-119">Если ошибка возникает во время асинхронной операции, **RDS. Значение ReadyState объекта DataControl** изменяется с **adcReadyStateLoaded** на **adcReadyStateComplete,** а значение свойства **Recordset** остается *Ничто*. [](readystate-property-rds.md)</span><span class="sxs-lookup"><span data-stu-id="a089d-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

