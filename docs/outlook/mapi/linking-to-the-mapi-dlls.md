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
ms.openlocfilehash: 0bce1d682057b81135d1684c40bc79e6710d4e2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809642"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="23471-103">Связывание с библиотеками DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="23471-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="23471-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23471-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23471-105">Клиентов MAPI можно связать библиотек MAPI неявно или явно с помощью функции Windows **LoadLibrary** и **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="23471-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="23471-106">Сведения о явно связанные библиотеки MAPI DLL см [ссылка на функции MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="23471-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="23471-107">MAPI предоставляет инструкции определения типа в MAPIX. Файл заголовка для каждого из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="23471-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="23471-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="23471-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="23471-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="23471-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="23471-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="23471-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="23471-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="23471-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="23471-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="23471-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="23471-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="23471-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="23471-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="23471-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="23471-115">Используйте эти определения типов правильно вызов соответствующих точек входа при связывании явно библиотек MAPI.</span><span class="sxs-lookup"><span data-stu-id="23471-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="23471-116">Поставщиков услуг может содержать функции не MAPI — функции, которые полностью не MAPI — в своей библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="23471-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="23471-117">Если необходимо использовать следующие компоненты, вызвать **LoadLibrary** перед использованием DLL-Библиотеку и **FreeLibrary** удаление библиотеки DLL из памяти после его использования.</span><span class="sxs-lookup"><span data-stu-id="23471-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="23471-118">Так как MAPI не знает не MAPI варианты использования поставщика услуг DLL-Библиотеку, нет гарантии, что библиотеки DLL будет доступно при необходимости.</span><span class="sxs-lookup"><span data-stu-id="23471-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="23471-119">MAPI освобождает поставщика услуг DLL при больше не все клиенты с активных сеансов, которые требуют его службы.</span><span class="sxs-lookup"><span data-stu-id="23471-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

