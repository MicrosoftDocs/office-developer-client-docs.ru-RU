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
# <a name="readystate-property-rds"></a><span data-ttu-id="6e06a-102">Свойство ReadyState (RDS)</span><span class="sxs-lookup"><span data-stu-id="6e06a-102">ReadyState property (RDS)</span></span>

<span data-ttu-id="6e06a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e06a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e06a-104">Показывает ход выполнения объекта " [элемент управления](datacontrol-object-rds.md) данными" при извлечении данных в объект [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6e06a-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6e06a-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6e06a-105">Settings and return values</span></span>

<span data-ttu-id="6e06a-106">Задает или возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6e06a-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e06a-107">Значение</span><span class="sxs-lookup"><span data-stu-id="6e06a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="6e06a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6e06a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e06a-109"><strong>Адкреадистателоадед</strong></span><span class="sxs-lookup"><span data-stu-id="6e06a-109"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="6e06a-110">Текущий запрос по-прежнему выполняется, и строки не извлекаются.</span><span class="sxs-lookup"><span data-stu-id="6e06a-110">The current query is still executing and no rows have been fetched.</span></span> <span data-ttu-id="6e06a-111"><strong>Набор записей</strong> объекта " <strong>элемент управления</strong> данных" недоступен для использования.</span><span class="sxs-lookup"><span data-stu-id="6e06a-111">The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e06a-112"><strong>Адкреадистатеинтерактиве</strong></span><span class="sxs-lookup"><span data-stu-id="6e06a-112"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="6e06a-113">Начальный набор строк, извлеченный текущим запросом, был сохранен в наборе <strong></strong> <strong>записей</strong> объекта данных и доступен для использования.</span><span class="sxs-lookup"><span data-stu-id="6e06a-113">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="6e06a-114">Остальные строки все еще выбираются.</span><span class="sxs-lookup"><span data-stu-id="6e06a-114">The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e06a-115"><strong>Адкреадистатекомплете</strong></span><span class="sxs-lookup"><span data-stu-id="6e06a-115"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="6e06a-116">Все строки, извлеченные текущим запросом, были сохранены в <strong></strong> <strong>наборе записей</strong> объекта данных и доступны для использования.</span><span class="sxs-lookup"><span data-stu-id="6e06a-116">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="6e06a-117">Это состояние также будет существовать, если операция прервана из-за ошибки или объект <strong>Recordset</strong> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="6e06a-117">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6e06a-118">Каждый исполняемый файл на стороне клиента, использующий эти константы, должен предоставлять объявления для них.</span><span class="sxs-lookup"><span data-stu-id="6e06a-118">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="6e06a-119">Вы можете вырезать и вставить объявления констант из файла Адквбс. Inc, расположенного в папке C:\Program Files\Common Филес\систем\мсадк.</span><span class="sxs-lookup"><span data-stu-id="6e06a-119">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e06a-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e06a-120">Remarks</span></span>

<span data-ttu-id="6e06a-121">Используйте событие [онреадистатечанже](onreadystatechange-event-rds.md) для отслеживания изменений в свойстве **ReadyState** во время асинхронной операции запроса.</span><span class="sxs-lookup"><span data-stu-id="6e06a-121">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation.</span></span> <span data-ttu-id="6e06a-122">Это более эффективно, чем периодическая проверка значения свойства.</span><span class="sxs-lookup"><span data-stu-id="6e06a-122">This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="6e06a-123">Если во время асинхронной операции возникает ошибка, свойство **ReadyState** изменяется на **Адкреадистатекомплете**, свойство [State](state-property-ado.md) изменяется с **адстатиксекутинг** на **адстатеклосед**, а объект **Recordset** Свойство [value](value-property-ado.md) объекта *не*остается.</span><span class="sxs-lookup"><span data-stu-id="6e06a-123">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

