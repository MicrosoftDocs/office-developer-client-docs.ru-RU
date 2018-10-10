---
title: The Microsoft Cursor Service for OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b84899cc4dd8a85cc48ab26057935c9ab150361
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482462"
---
# <a name="the-microsoft-cursor-service-for-ole-db"></a><span data-ttu-id="c4365-102">The Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="c4365-102">The Microsoft Cursor Service for OLE DB</span></span>


<span data-ttu-id="c4365-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4365-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4365-104">При установке курсора со стороны клиента, или задайте для свойства **CursorLocation** значение **adUseClient**, вызовах службы Microsoft курсора для OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c4365-104">When you select a client-side cursor, or set the **CursorLocation** property to **adUseClient**, you are invoking the Microsoft Cursor Service for OLE DB.</span></span> <span data-ttu-id="c4365-105">Можно также увидеть ссылки «Клиента курсора обработчик», который является по сути то же самое в контексте ADO.</span><span class="sxs-lookup"><span data-stu-id="c4365-105">You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO.</span></span> <span data-ttu-id="c4365-106">Эта служба используется в качестве дополнения функции поддержки курсора поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="c4365-106">This service supplements the cursor-support functions of data providers.</span></span> <span data-ttu-id="c4365-107">В результате воспринимает относительно универсальный код функции из всех поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="c4365-107">As a result, you can perceive relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="c4365-108">Служба курсора для OLE DB делает доступными динамические свойства и улучшающий поведение некоторых методов.</span><span class="sxs-lookup"><span data-stu-id="c4365-108">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods.</span></span> <span data-ttu-id="c4365-109">К примеру динамическое свойство **оптимизировать** позволяет создавать временных индексов для облегчения определенные операции, такие как метод **поиска** .</span><span class="sxs-lookup"><span data-stu-id="c4365-109">For example, the **Optimize** dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the **Find** method.</span></span>

<span data-ttu-id="c4365-110">Служба курсора обеспечивает поддержку для пакетного обновления во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="c4365-110">The Cursor Service enables support for batch updating in all cases.</span></span> <span data-ttu-id="c4365-111">Также более производительные курсора типов, таких как динамические курсоры моделирует, когда поставщик данных может поддерживать только менее производительные курсоры, такие как статические курсоры.</span><span class="sxs-lookup"><span data-stu-id="c4365-111">It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

