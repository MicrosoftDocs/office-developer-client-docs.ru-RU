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
ms.openlocfilehash: f182610f9cf4874cc18c409960e1f8b23f853d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574828"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="32d13-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32d13-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="32d13-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32d13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32d13-105">Позволяет Microsoft Outlook 2010 и Microsoft Outlook 2013 решения узнать, если вложение считается небезопасные и заблокированные для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="32d13-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32d13-106">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="32d13-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="32d13-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="32d13-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="32d13-108">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="32d13-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="32d13-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="32d13-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="32d13-110">Проверяет, если указанное вложение не заблокирован по Outlook 2010 или Outlook 2013 для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="32d13-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32d13-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="32d13-111">Remarks</span></span>

<span data-ttu-id="32d13-112">Решения для Outlook 2010 и Outlook 2013 можно запросить этот интерфейс, чтобы увидеть, если вложения блокируется.</span><span class="sxs-lookup"><span data-stu-id="32d13-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="32d13-113">Вложения, которые блокируются по Outlook 2010 или Outlook 2013 различаться в зависимости от того, как был настроен Outlook 2010 или Outlook 2013 и политики, примененные администратора.</span><span class="sxs-lookup"><span data-stu-id="32d13-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32d13-114">См. также</span><span class="sxs-lookup"><span data-stu-id="32d13-114">See also</span></span>



[<span data-ttu-id="32d13-115">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="32d13-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="32d13-116">Проверка блокировки вложения</span><span class="sxs-lookup"><span data-stu-id="32d13-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

