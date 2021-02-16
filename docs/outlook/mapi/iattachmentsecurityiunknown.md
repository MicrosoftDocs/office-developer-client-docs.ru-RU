---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411416"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="5950c-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5950c-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="5950c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5950c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5950c-105">Позволяет Microsoft Outlook 2010, русская версия и решения Microsoft Outlook 2013, чтобы узнать, считается ли вложение небезопасным и заблокировано для просмотра и индексации.</span><span class="sxs-lookup"><span data-stu-id="5950c-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5950c-106">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5950c-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5950c-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="5950c-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5950c-108">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="5950c-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5950c-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="5950c-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="5950c-110">Проверяет, заблокировано ли указанное вложение в Outlook 2010 или Outlook 2013 для просмотра и индексации.</span><span class="sxs-lookup"><span data-stu-id="5950c-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5950c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="5950c-111">Remarks</span></span>

<span data-ttu-id="5950c-112">Решения Outlook 2010 и Outlook 2013 могут запрашивать этот интерфейс, чтобы узнать, заблокировано ли вложение.</span><span class="sxs-lookup"><span data-stu-id="5950c-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="5950c-113">Вложения, заблокированные Outlook 2010 или Outlook 2013, зависят от настройки Outlook 2010 или Outlook 2013 и примененных администратором политик.</span><span class="sxs-lookup"><span data-stu-id="5950c-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5950c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="5950c-114">See also</span></span>



[<span data-ttu-id="5950c-115">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="5950c-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5950c-116">Проверка блокировки вложения</span><span class="sxs-lookup"><span data-stu-id="5950c-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

