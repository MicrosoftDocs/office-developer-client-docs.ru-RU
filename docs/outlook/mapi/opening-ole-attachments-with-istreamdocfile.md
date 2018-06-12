---
title: Открытие вложения OLE с IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Последнее изменение: 06 июля 2012 г.'
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810079"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="ecba3-103">Открытие вложения OLE с IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="ecba3-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="ecba3-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecba3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecba3-105">При открытии вложения объектов OLE, с помощью интерфейса **IStreamDocfile** , а не [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) или [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ecba3-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="ecba3-106">**IStreamDocfile** предоставляет прямой доступ к объекту с помощью структурированного хранилища, устраняя необходимость выполнения операции копирования и снизить число дополнительную нагрузку.</span><span class="sxs-lookup"><span data-stu-id="ecba3-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="ecba3-107">**IStreamDocfile** — это реализации **IStream** с содержимым потока, обязательно быть в формате структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="ecba3-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="ecba3-108">**IStreamDocfile** реализуется поставщиками хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ecba3-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

