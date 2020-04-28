---
title: The Microsoft Cursor Service for OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314359"
---
# <a name="microsoft-cursor-service-for-ole-db"></a><span data-ttu-id="65fea-102">Служба курсора (Майкрософт) для OLE DB</span><span class="sxs-lookup"><span data-stu-id="65fea-102">Microsoft Cursor Service for OLE DB</span></span>


<span data-ttu-id="65fea-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65fea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65fea-104">При выборе клиентского курсора или задании свойства **CursorLocation** равным **адусеклиент**, вызывается служба Microsoft Cursor Cursor для OLE DB.</span><span class="sxs-lookup"><span data-stu-id="65fea-104">When you select a client-side cursor, or set the **CursorLocation** property to **adUseClient**, you are invoking the Microsoft Cursor Service for OLE DB.</span></span> <span data-ttu-id="65fea-105">Кроме того, вы также можете увидеть ссылки на "обработчик курсоров клиента", который по сути является тем же, что и в контексте ADO.</span><span class="sxs-lookup"><span data-stu-id="65fea-105">You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO.</span></span> <span data-ttu-id="65fea-106">Эта служба дополняет функции поддержки курсора поставщиками данных.</span><span class="sxs-lookup"><span data-stu-id="65fea-106">This service supplements the cursor-support functions of data providers.</span></span> <span data-ttu-id="65fea-107">В результате вы можете воспринимать относительно единообразные функциональные возможности всех поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="65fea-107">As a result, you can perceive relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="65fea-108">Служба курсора для OLE DB делает динамические свойства доступными и расширяет поведение определенных методов.</span><span class="sxs-lookup"><span data-stu-id="65fea-108">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods.</span></span> <span data-ttu-id="65fea-109">Например, динамическое свойство **optimize** позволяет создавать временные индексы для упрощения определенных операций, например метода **Find** .</span><span class="sxs-lookup"><span data-stu-id="65fea-109">For example, the **Optimize** dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the **Find** method.</span></span>

<span data-ttu-id="65fea-110">Служба курсоров обеспечивает поддержку пакетного обновления во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="65fea-110">The Cursor Service enables support for batch updating in all cases.</span></span> <span data-ttu-id="65fea-111">Он также имитирует дополнительные типы курсоров, например динамические курсоры, когда поставщик данных может предоставлять только менее доступные курсоры, например статические курсоры.</span><span class="sxs-lookup"><span data-stu-id="65fea-111">It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

