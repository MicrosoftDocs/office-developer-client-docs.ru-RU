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
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808768"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="361a4-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="361a4-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="361a4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="361a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="361a4-105">Позволяет Microsoft Outlook 2010 и Microsoft Outlook 2013 решения узнать, если вложение считается небезопасные и заблокированные для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="361a4-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="361a4-106">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="361a4-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="361a4-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="361a4-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="361a4-108">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="361a4-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="361a4-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="361a4-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="361a4-110">Проверяет, если указанное вложение не заблокирован по Outlook 2010 или Outlook 2013 для просмотра и индексирования.</span><span class="sxs-lookup"><span data-stu-id="361a4-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="361a4-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="361a4-111">Remarks</span></span>

<span data-ttu-id="361a4-112">Решения для Outlook 2010 и Outlook 2013 можно запросить этот интерфейс, чтобы увидеть, если вложения блокируется.</span><span class="sxs-lookup"><span data-stu-id="361a4-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="361a4-113">Вложения, которые блокируются по Outlook 2010 или Outlook 2013 различаться в зависимости от того, как был настроен Outlook 2010 или Outlook 2013 и политики, примененные администратора.</span><span class="sxs-lookup"><span data-stu-id="361a4-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="361a4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="361a4-114">See also</span></span>



[<span data-ttu-id="361a4-115">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="361a4-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="361a4-116">Проверка блокировки вложения</span><span class="sxs-lookup"><span data-stu-id="361a4-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

