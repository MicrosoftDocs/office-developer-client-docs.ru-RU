---
title: Связывание с библиотеками DLL MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 428e92dd783368374fa07c8df9629d60e83dd217
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582030"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="19113-103">Связывание с библиотеками DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="19113-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="19113-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19113-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19113-105">Клиентов MAPI можно связать библиотек MAPI неявно или явно с помощью функции Windows **LoadLibrary** и **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="19113-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="19113-106">Сведения о явно связанные библиотеки MAPI DLL см [ссылка на функции MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="19113-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="19113-107">MAPI предоставляет инструкции определения типа в MAPIX. Файл заголовка для каждого из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="19113-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="19113-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="19113-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="19113-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="19113-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="19113-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="19113-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="19113-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="19113-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="19113-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="19113-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="19113-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="19113-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="19113-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="19113-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="19113-115">Используйте эти определения типов правильно вызов соответствующих точек входа при связывании явно библиотек MAPI.</span><span class="sxs-lookup"><span data-stu-id="19113-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="19113-116">Поставщиков услуг может содержать функции не MAPI — функции, которые полностью не MAPI — в своей библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="19113-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="19113-117">Если необходимо использовать следующие компоненты, вызвать **LoadLibrary** перед использованием DLL-Библиотеку и **FreeLibrary** удаление библиотеки DLL из памяти после его использования.</span><span class="sxs-lookup"><span data-stu-id="19113-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="19113-118">Так как MAPI не знает не MAPI варианты использования поставщика услуг DLL-Библиотеку, нет гарантии, что библиотеки DLL будет доступно при необходимости.</span><span class="sxs-lookup"><span data-stu-id="19113-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="19113-119">MAPI освобождает поставщика услуг DLL при больше не все клиенты с активных сеансов, которые требуют его службы.</span><span class="sxs-lookup"><span data-stu-id="19113-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

