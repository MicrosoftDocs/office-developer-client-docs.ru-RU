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
# <a name="executeoptions-property-rds"></a><span data-ttu-id="5c8fd-102">Свойство ExecuteOptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="5c8fd-102">ExecuteOptions property (RDS)</span></span>


<span data-ttu-id="5c8fd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c8fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c8fd-104">Указывает, включено ли асинхронное выполнение.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5c8fd-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5c8fd-105">Settings and return values</span></span>

<span data-ttu-id="5c8fd-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c8fd-107">Константа</span><span class="sxs-lookup"><span data-stu-id="5c8fd-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="5c8fd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5c8fd-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c8fd-109"><strong>Адцексексинк</strong></span><span class="sxs-lookup"><span data-stu-id="5c8fd-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="5c8fd-110">Выполняет следующее обновление <a href="recordset-object-ado.md">набора записей</a> в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c8fd-111"><strong>Адцексекасинк</strong></span><span class="sxs-lookup"><span data-stu-id="5c8fd-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="5c8fd-112">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-112">Default.</span></span> <span data-ttu-id="5c8fd-113">Асинхронно выполняет следующее обновление объекта <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="5c8fd-113">Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5c8fd-114">Каждый исполняемый файл на стороне клиента, использующий эти константы, должен предоставлять объявления для них.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-114">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="5c8fd-115">Вы можете вырезать и вставить объявления констант из файла Адквбс. Inc, расположенного в папке C:\Program Files\Common Филес\систем\мсадк.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-115">You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8fd-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5c8fd-116">Remarks</span></span>

<span data-ttu-id="5c8fd-117">Если для **ExecuteOptions** задано значение **адцексекасинк**, асинхронно выполняется следующий вызов **обновления** в [RDS. ](datacontrol-object-rds.md) **Набор записей**объекта DataObject.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="5c8fd-118">Если вы попытаетесь вызвать [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md)или [Recordset](recordset-sourcerecordset-properties-rds.md) , в то время как другая асинхронная операция, которая может изменить [RDS. ](datacontrol-object-rds.md)Выполняется **набор записей** объекта DataObject, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="5c8fd-119">Если во время асинхронной операции возникает ошибка, то \*\*RDS. \*\*Изменение значения свойства [ReadyState](readystate-property-rds.md) объекта **адкреадистателоадед** на **Адкреадистатекомплете**, а значение свойства **Recordset** *не*остается.</span><span class="sxs-lookup"><span data-stu-id="5c8fd-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

