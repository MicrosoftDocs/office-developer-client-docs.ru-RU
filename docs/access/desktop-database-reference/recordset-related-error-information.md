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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307618"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="b1b24-102">Сведения об ошибках, связанных с наборами записей</span><span class="sxs-lookup"><span data-stu-id="b1b24-102">Recordset-related error information</span></span>

<span data-ttu-id="b1b24-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1b24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1b24-104">Во время пакетной обработки свойство **Status** объекта **Recordset** предоставляет сведения об отдельных записях в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="b1b24-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="b1b24-105">Перед пакетным обновлением свойство **Status** of the **Recordset** отображает сведения о записях, которые будут добавлены, изменены и удалены.</span><span class="sxs-lookup"><span data-stu-id="b1b24-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="b1b24-106">После того как был вызван **UpdateBatch,** свойство **Status** указывает на успешность или сбой операции.</span><span class="sxs-lookup"><span data-stu-id="b1b24-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="b1b24-107">При переходе от записи к записи в **Наборе** записей значение свойства **Status** изменяется для описания состояния текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b1b24-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

