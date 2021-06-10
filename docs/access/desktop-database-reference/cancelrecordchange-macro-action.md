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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296656"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="98134-102">Макрокоманда CancelRecordChange</span><span class="sxs-lookup"><span data-stu-id="98134-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="98134-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98134-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98134-104">Действие **CancelRecordChange** можно использовать для отмены изменений, примененных к записи в блоке данных **[CreateRecord](createrecord-data-block.md)** или **[EditRecord](editrecord-data-block.md)** до совершения изменений.</span><span class="sxs-lookup"><span data-stu-id="98134-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="98134-105">Действие **CancelRecordChange** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="98134-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="98134-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="98134-106">Remarks</span></span>

<span data-ttu-id="98134-107">При вызове **действия CancelRecordChange** блок **данных CreateRecord** или **EditRecord** немедленно выходит.</span><span class="sxs-lookup"><span data-stu-id="98134-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

