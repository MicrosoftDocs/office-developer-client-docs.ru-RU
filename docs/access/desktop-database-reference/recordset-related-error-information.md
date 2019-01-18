---
title: Сведения об ошибках, связанных с наборами записей
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 12a67657d5543aac22a49690256b0410a2b901bd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708902"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="75257-102">Сведения об ошибках, связанных с наборами записей</span><span class="sxs-lookup"><span data-stu-id="75257-102">Recordset-related error information</span></span>

<span data-ttu-id="75257-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75257-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75257-104">Во время пакетной обработки свойство **Status** объекта **набора записей** сведения об отдельных записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="75257-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="75257-105">Перед обновлением пакета, свойство **Status** **записей** отражает сведения о записях для добавления, изменения и удаления.</span><span class="sxs-lookup"><span data-stu-id="75257-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="75257-106">После вызова **UpdateBatch** свойство **Status** указывает успешное или неудачное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="75257-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="75257-107">При перемещении по записям в **набор записей,** значение изменения свойств **состояния** для описания состояние текущей записи.</span><span class="sxs-lookup"><span data-stu-id="75257-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

