---
title: Recordset-Related Error Information
TOCTitle: Recordset-Related Error Information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62f9a6d235b6c06ad8e7fa49d7b89960fd1ad2b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482074"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="29b48-102">Recordset-Related Error Information</span><span class="sxs-lookup"><span data-stu-id="29b48-102">Recordset-Related Error Information</span></span>


<span data-ttu-id="29b48-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="29b48-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="29b48-104">Во время пакетной обработки свойство **Status** объекта **набора записей** сведения об отдельных записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="29b48-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="29b48-105">Перед обновлением пакета, свойство **Status** **записей** отражает сведения о записях для добавления, изменения и удаления.</span><span class="sxs-lookup"><span data-stu-id="29b48-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="29b48-106">После вызова **UpdateBatch** свойство **Status** указывает успешное или неудачное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="29b48-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="29b48-107">При перемещении по записям в **набор записей,** значение изменения свойств **состояния** для описания состояние текущей записи.</span><span class="sxs-lookup"><span data-stu-id="29b48-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

