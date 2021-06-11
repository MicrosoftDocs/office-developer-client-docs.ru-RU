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
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419305"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="1e572-103">Связывание с библиотеками DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="1e572-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="1e572-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e572-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e572-105">Клиенты MAPI могут связаться с DLLs MAPI неявно или явно с помощью функций **Windows LoadLibrary** и **GetProcAddress.**</span><span class="sxs-lookup"><span data-stu-id="1e572-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="1e572-106">Сведения о явной привязке DLLs MAPI см. в ссылке [на функции MAPI.](how-to-link-to-mapi-functions.md)</span><span class="sxs-lookup"><span data-stu-id="1e572-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="1e572-107">MAPI предоставляет утверждения определения типов в MAPIX. Файл H-загона для каждой из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="1e572-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="1e572-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1e572-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="1e572-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="1e572-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="1e572-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="1e572-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="1e572-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1e572-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1e572-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1e572-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="1e572-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1e572-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1e572-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="1e572-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="1e572-115">Используйте эти определения типа, чтобы правильно вызывать соответствующие точки входа, если вы явно ссылались на DLLs MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e572-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="1e572-116">Поставщики услуг могут содержать функции, не относящиеся к MAPI, — функции, совершенно не связанные с MAPI, в их DLL.</span><span class="sxs-lookup"><span data-stu-id="1e572-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="1e572-117">Если необходимо использовать эти функции, прежде чем использовать DLL и **FreeLibrary,** позвоните **в LoadLibrary,** чтобы удалить DLL из памяти после его использования.</span><span class="sxs-lookup"><span data-stu-id="1e572-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="1e572-118">Так как MAPI не знает о том, что поставщик услуг DLL не использует не MAPI, нет никакой гарантии, что DLL будет доступен при необходимости.</span><span class="sxs-lookup"><span data-stu-id="1e572-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="1e572-119">MAPI выпускает DLL поставщика услуг, когда больше нет клиентов с активными сеансами, которые требуют его служб.</span><span class="sxs-lookup"><span data-stu-id="1e572-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

