---
title: ExecuteOptions Property (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 641e7942f5336f230d396db7e06b9d0601645cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480239"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="1a4a4-102">ExecuteOptions Property (RDS)</span><span class="sxs-lookup"><span data-stu-id="1a4a4-102">ExecuteOptions Property (RDS)</span></span>


<span data-ttu-id="1a4a4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a4a4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1a4a4-104">Указывает, включена ли асинхронное выполнение.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1a4a4-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1a4a4-105">Settings and Return Values</span></span>

<span data-ttu-id="1a4a4-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a4a4-107">Константа</span><span class="sxs-lookup"><span data-stu-id="1a4a4-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="1a4a4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1a4a4-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a4a4-109"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="1a4a4-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="1a4a4-110">Синхронно выполняет следующего обновления <a href="recordset-object-ado.md">набора записей</a> .</span><span class="sxs-lookup"><span data-stu-id="1a4a4-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a4a4-111"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="1a4a4-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="1a4a4-112">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-112">Default.</span></span> <span data-ttu-id="1a4a4-113">Асинхронно выполняет следующего обновления <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a4a4-113">Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="1a4a4-114">Каждый исполняемый файл со стороны клиента, который использует эти константы необходимо предоставить объявления для них.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-114">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="1a4a4-115">Можно вырежьте и вставьте объявлений констант, которые будут из файла Adcvbs.inc, находящийся в папке C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-115">You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="1a4a4-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a4a4-116">Remarks</span></span>

<span data-ttu-id="1a4a4-117">Если **ExecuteOptions** **adcExecAsync**, затем это асинхронно выполняет следующий вызов **обновления** на [RDS. DataControl](datacontrol-object-rds.md) объекта **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="1a4a4-118">При попытке вызова [Сброс](reset-method-rds.md), [обновление](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md)или [набора записей](recordset-sourcerecordset-properties-rds.md) при другой асинхронной операции, который может изменяться [RDS. DataControl](datacontrol-object-rds.md) объекта **набора записей** выполняется, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="1a4a4-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="1a4a4-119">При возникновении ошибки во время выполнения асинхронной операции, **RDS. DataControl** значения [ReadyState](readystate-property-rds.md) объекта изменяется с **adcReadyStateLoaded** на **adcReadyStateComplete**и *ничего не*остается значение свойства **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="1a4a4-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

