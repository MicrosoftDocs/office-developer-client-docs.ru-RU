---
title: Макрокоманда CancelRecordChange
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb414837696eecc028d864c1efa9f74251f596a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919334"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="2981f-102">Макрокоманда CancelRecordChange</span><span class="sxs-lookup"><span data-stu-id="2981f-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="2981f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2981f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2981f-104">Отмена изменения, примененные к записи блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** до изменения, можно использовать действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="2981f-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="2981f-105">Действие **CancelRecordChange** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="2981f-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="2981f-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="2981f-106">Remarks</span></span>

<span data-ttu-id="2981f-107">При вызове действие **CancelRecordChange** блок данных **СоздатьЗапись** или **ИзменитьЗапись** немедленно прекращается.</span><span class="sxs-lookup"><span data-stu-id="2981f-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

