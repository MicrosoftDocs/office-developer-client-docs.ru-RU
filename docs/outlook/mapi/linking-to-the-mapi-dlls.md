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
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="3af1e-103">Связывание с библиотеками DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="3af1e-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="3af1e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3af1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3af1e-105">Клиенты MAPI могут связываться с DLL MAPI неявно или явным образом с помощью функций Windows **LoadLibrary** и **GetProcAddress.**</span><span class="sxs-lookup"><span data-stu-id="3af1e-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="3af1e-106">Сведения об явной привязке DLL MAPI см. в ссылке [на функции MAPI.](how-to-link-to-mapi-functions.md)</span><span class="sxs-lookup"><span data-stu-id="3af1e-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="3af1e-107">MAPI предоставляет определения типов в MAPIX. Файл h-загона для каждой из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="3af1e-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="3af1e-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="3af1e-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="3af1e-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="3af1e-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="3af1e-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="3af1e-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="3af1e-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3af1e-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3af1e-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="3af1e-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="3af1e-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3af1e-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3af1e-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="3af1e-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="3af1e-115">Используйте эти определения типов, чтобы правильно вызывать соответствующие точки входа, если вы явно ссылались на DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="3af1e-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="3af1e-116">Поставщики услуг могут содержать в своей DLL функции, не связанные с MAPI.</span><span class="sxs-lookup"><span data-stu-id="3af1e-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="3af1e-117">Если необходимо использовать эти функции, вызовите **LoadLibrary** перед использованием DLL и **FreeLibrary,** чтобы удалить DLL из памяти после ее использования.</span><span class="sxs-lookup"><span data-stu-id="3af1e-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="3af1e-118">Поскольку MAPI не знает о том, как DLL поставщика услуг не используется mapI, нет гарантии, что она будет доступна при необходимости.</span><span class="sxs-lookup"><span data-stu-id="3af1e-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="3af1e-119">MAPI выпускает DLL поставщика услуг, если больше нет клиентов с активными сеансами, требуя его служб.</span><span class="sxs-lookup"><span data-stu-id="3af1e-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

