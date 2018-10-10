---
title: CancelRecordChange Macro Action
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fe474f9ba7250e3225bc73460c6d192800c861b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481296"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="e926c-102">CancelRecordChange Macro Action</span><span class="sxs-lookup"><span data-stu-id="e926c-102">CancelRecordChange Macro Action</span></span>


<span data-ttu-id="e926c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e926c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e926c-104">Отмена изменения, примененные к записи блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** до изменения, можно использовать действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="e926c-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e926c-105">Действие <STRONG>CancelRecordChange</STRONG> доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="e926c-105">The <STRONG>CancelRecordChange</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="e926c-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="e926c-106">Remarks</span></span>

<span data-ttu-id="e926c-107">При вызове действие **CancelRecordChange** блок данных **СоздатьЗапись** или **ИзменитьЗапись** немедленно прекращается.</span><span class="sxs-lookup"><span data-stu-id="e926c-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

