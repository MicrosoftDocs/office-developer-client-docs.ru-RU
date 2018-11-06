---
title: Свойство ReadyState (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62229a06405c1c7dabc9826b8b03823df5cc1f05
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996631"
---
# <a name="readystate-property-rds"></a><span data-ttu-id="25882-102">Свойство ReadyState (RDS)</span><span class="sxs-lookup"><span data-stu-id="25882-102">ReadyState property (RDS)</span></span>

<span data-ttu-id="25882-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25882-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25882-104">Индикатор выполнения объекта [DataControl](datacontrol-object-rds.md) при извлечении данных в его объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="25882-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="25882-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="25882-105">Settings and return values</span></span>

<span data-ttu-id="25882-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="25882-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25882-107">Значение</span><span class="sxs-lookup"><span data-stu-id="25882-107">Value</span></span></p></th>
<th><p><span data-ttu-id="25882-108">Описание</span><span class="sxs-lookup"><span data-stu-id="25882-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25882-109"><strong>adcReadyStateLoaded</strong></span><span class="sxs-lookup"><span data-stu-id="25882-109"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="25882-110">Текущий запрос по-прежнему выполняется и строки не выбраны.</span><span class="sxs-lookup"><span data-stu-id="25882-110">The current query is still executing and no rows have been fetched.</span></span> <span data-ttu-id="25882-111">Объект <strong>DataControl</strong> <strong>записей</strong> недоступен для использования.</span><span class="sxs-lookup"><span data-stu-id="25882-111">The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25882-112"><strong>adcReadyStateInteractive</strong></span><span class="sxs-lookup"><span data-stu-id="25882-112"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="25882-113">Начальный набор строк, которые извлекаются с текущего запроса был сохранен в объекте <strong>DataControl</strong> <strong>записей</strong> и доступны для использования.</span><span class="sxs-lookup"><span data-stu-id="25882-113">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="25882-114">Оставшиеся строки по-прежнему извлечении.</span><span class="sxs-lookup"><span data-stu-id="25882-114">The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25882-115"><strong>adcReadyStateComplete</strong></span><span class="sxs-lookup"><span data-stu-id="25882-115"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="25882-116">Все полученные текущего запроса строки хранятся в объекте <strong>DataControl</strong> <strong>записей</strong> и доступны для использования.</span><span class="sxs-lookup"><span data-stu-id="25882-116">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="25882-117">Это состояние также будет существовать, если операция прервана из-за ошибки или объекта <strong>набора записей</strong> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="25882-117">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="25882-118">Каждый исполняемый файл со стороны клиента, который использует эти константы необходимо предоставить объявления для них.</span><span class="sxs-lookup"><span data-stu-id="25882-118">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="25882-119">Можно вырежьте и вставьте объявлений констант из файла Adcvbs.inc, находящийся в папке C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="25882-119">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="25882-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="25882-120">Remarks</span></span>

<span data-ttu-id="25882-121">Событие [onReadyStateChange](onreadystatechange-event-rds.md) используется для отслеживания изменений в свойстве **ReadyState** во время операции асинхронного запроса.</span><span class="sxs-lookup"><span data-stu-id="25882-121">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation.</span></span> <span data-ttu-id="25882-122">Это эффективнее, чем периодически проверки значения свойства.</span><span class="sxs-lookup"><span data-stu-id="25882-122">This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="25882-123">При возникновении ошибки во время асинхронной операции, изменения свойств **ReadyState** **adcReadyStateComplete**свойство [State](state-property-ado.md) изменяется с **adStateExecuting** **adStateClosed**и **записей** Свойство [Value](value-property-ado.md) объекта остается *значение Nothing*.</span><span class="sxs-lookup"><span data-stu-id="25882-123">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

