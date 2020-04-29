---
title: Иаттачментсекурити IUnknown
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
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="93245-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="93245-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="93245-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93245-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93245-105">Позволяет решениям Microsoft Outlook 2010 и Microsoft Outlook 2013 проверить, считается ли вложение небезопасным и заблокировано для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="93245-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93245-106">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="93245-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="93245-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="93245-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="93245-108">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="93245-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="93245-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="93245-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="93245-110">Проверяет, заблокировано ли заданное вложение Outlook 2010 или Outlook 2013 для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="93245-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93245-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="93245-111">Remarks</span></span>

<span data-ttu-id="93245-112">Решения Outlook 2010 и Outlook 2013 могут запрашивать этот интерфейс, чтобы проверить, заблокировано ли вложение.</span><span class="sxs-lookup"><span data-stu-id="93245-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="93245-113">Вложения, блокируемые Outlook 2010 или Outlook 2013, зависят от того, как настроены Outlook 2010 или Outlook 2013, а также политики, примененные администратором.</span><span class="sxs-lookup"><span data-stu-id="93245-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93245-114">См. также</span><span class="sxs-lookup"><span data-stu-id="93245-114">See also</span></span>



[<span data-ttu-id="93245-115">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="93245-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="93245-116">Проверка блокировки вложения</span><span class="sxs-lookup"><span data-stu-id="93245-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

