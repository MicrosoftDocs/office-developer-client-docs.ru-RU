---
title: Свойство ReadyState (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300821"
---
# <a name="readystate-property-rds"></a><span data-ttu-id="59e85-102">Свойство ReadyState (RDS)</span><span class="sxs-lookup"><span data-stu-id="59e85-102">ReadyState property (RDS)</span></span>

<span data-ttu-id="59e85-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59e85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59e85-104">Указывает ход выполнения объекта [DataControl](datacontrol-object-rds.md) при извлечении данных в объект [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="59e85-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="59e85-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="59e85-105">Settings and return values</span></span>

<span data-ttu-id="59e85-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="59e85-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59e85-107">Значение</span><span class="sxs-lookup"><span data-stu-id="59e85-107">Value</span></span></p></th>
<th><p><span data-ttu-id="59e85-108">Описание</span><span class="sxs-lookup"><span data-stu-id="59e85-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59e85-109"><strong>adcReadyStateLoaded</strong></span><span class="sxs-lookup"><span data-stu-id="59e85-109"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="59e85-110">Текущий запрос по-прежнему выполняется, и строки не были извлечены.</span><span class="sxs-lookup"><span data-stu-id="59e85-110">The current query is still executing and no rows have been fetched.</span></span> <span data-ttu-id="59e85-111">Набор записей объекта <strong>DataControl</strong> не доступен для использования. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="59e85-111">The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59e85-112"><strong>adcReadyStateInteractive</strong></span><span class="sxs-lookup"><span data-stu-id="59e85-112"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="59e85-113">Начальный набор строк, полученных текущим запросом, хранится в наборе <strong></strong> записей объекта <strong>DataControl</strong> и доступен для использования.</span><span class="sxs-lookup"><span data-stu-id="59e85-113">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="59e85-114">Остальные строки по-прежнему извлекаются.</span><span class="sxs-lookup"><span data-stu-id="59e85-114">The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59e85-115"><strong>adcReadyStateComplete</strong></span><span class="sxs-lookup"><span data-stu-id="59e85-115"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="59e85-116">Все строки, извлеченные текущим запросом, хранятся в наборе записей объекта <strong>DataControl</strong> и доступны для использования. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="59e85-116">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="59e85-117">Это состояние также будет существовать, если операция прерывается из-за ошибки или если объект <strong>Recordset</strong> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="59e85-117">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="59e85-118">Каждый исполняемый клиентский файл, использующий эти константы, должен предоставлять для них объявления.</span><span class="sxs-lookup"><span data-stu-id="59e85-118">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="59e85-119">Вы можете вырезать и ввести нужные постоянные объявления из файла Adcvbs.inc, расположенного в папке C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="59e85-119">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e85-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="59e85-120">Remarks</span></span>

<span data-ttu-id="59e85-121">Используйте [событие onReadyStateChange](onreadystatechange-event-rds.md) для мониторинга изменений свойства **ReadyState** во время асинхронной операции запроса.</span><span class="sxs-lookup"><span data-stu-id="59e85-121">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation.</span></span> <span data-ttu-id="59e85-122">Это эффективнее, чем периодические проверки значения свойства.</span><span class="sxs-lookup"><span data-stu-id="59e85-122">This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="59e85-123">Если ошибка возникает во время асинхронной операции, свойство **ReadyState** изменяется на [](value-property-ado.md) **adcReadyStateComplete,** свойство состояния меняется от **adStateExecuting до adStateClosed,** а свойство Значение объекта **Recordset** остается nothing *.* [](state-property-ado.md) </span><span class="sxs-lookup"><span data-stu-id="59e85-123">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

