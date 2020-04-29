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
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="9caa8-103">Связывание с библиотеками DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="9caa8-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="9caa8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9caa8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9caa8-105">Клиенты MAPI могут связываться с библиотеками MAPI неявным образом или явным образом с помощью функций Windows, **LoadLibrary** и **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="9caa8-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="9caa8-106">Сведения о явном связывании библиотек DLL MAPI приведены [в статье ссылки на функции MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9caa8-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="9caa8-107">MAPI предоставляет операторы определения типов в МАПИКС. H файл заголовков для каждой из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="9caa8-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="9caa8-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="9caa8-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="9caa8-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="9caa8-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="9caa8-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="9caa8-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="9caa8-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9caa8-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9caa8-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="9caa8-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="9caa8-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9caa8-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9caa8-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="9caa8-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="9caa8-115">Используйте эти определения типов, чтобы правильно вызывать соответствующие точки входа, если вы явно связываетесь с библиотеками MAPI.</span><span class="sxs-lookup"><span data-stu-id="9caa8-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="9caa8-116">Поставщики услуг могут содержать функции, не связанные с MAPI, — функции, полностью несвязанные с MAPI, в их DLL-библиотеках.</span><span class="sxs-lookup"><span data-stu-id="9caa8-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="9caa8-117">Если вам нужно использовать эти функции, вызовите **LoadLibrary** перед использованием DLL и **FreeLibrary** , чтобы удалить библиотеку DLL из памяти после ее использования.</span><span class="sxs-lookup"><span data-stu-id="9caa8-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="9caa8-118">Так как MAPI не знает об использовании библиотеки DLL поставщика услуг, отличной от MAPI, не гарантируется, что библиотека DLL будет доступна при необходимости.</span><span class="sxs-lookup"><span data-stu-id="9caa8-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="9caa8-119">MAPI освобождает библиотеку DLL поставщика услуг, когда больше нет клиентов с активными сеансами, для которых требуются службы.</span><span class="sxs-lookup"><span data-stu-id="9caa8-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

