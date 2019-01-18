---
title: Макрокоманда CancelRecordChange
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718545"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="5b6e1-102">Макрокоманда CancelRecordChange</span><span class="sxs-lookup"><span data-stu-id="5b6e1-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="5b6e1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b6e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b6e1-104">Отмена изменения, примененные к записи блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** до изменения, можно использовать действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="5b6e1-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="5b6e1-105">Действие **CancelRecordChange** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="5b6e1-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="5b6e1-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="5b6e1-106">Remarks</span></span>

<span data-ttu-id="5b6e1-107">При вызове действие **CancelRecordChange** блок данных **СоздатьЗапись** или **ИзменитьЗапись** немедленно прекращается.</span><span class="sxs-lookup"><span data-stu-id="5b6e1-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

