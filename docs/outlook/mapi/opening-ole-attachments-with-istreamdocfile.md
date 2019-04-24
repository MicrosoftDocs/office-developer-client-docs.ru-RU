---
title: Открытие вложений OLE с помощью IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Дата последнего изменения: 06 июля, 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326231"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="6edc0-103">Открытие вложений OLE с помощью IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="6edc0-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="6edc0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6edc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6edc0-105">При открытии вложения объекта OLE используйте интерфейс **помощью istreamdocfile** , а не [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) или [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6edc0-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="6edc0-106">**Помощью istreamdocfile** обеспечивает прямой доступ к объекту с помощью структурированного хранилища, избавляя от необходимости выполнять операцию копирования и сокращать издержки.</span><span class="sxs-lookup"><span data-stu-id="6edc0-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="6edc0-107">**Помощью istreamdocfile** — это конкретная реализация **IStream** с содержимым потока, которое гарантированно форматируется как структурированное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6edc0-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="6edc0-108">**Помощью istreamdocfile** реализуется поставщиками хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6edc0-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

