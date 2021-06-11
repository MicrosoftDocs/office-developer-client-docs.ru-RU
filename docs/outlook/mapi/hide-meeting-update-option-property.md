---
title: Скрыть свойство параметра Обновления собрания
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412102"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="fa7f6-103">Скрыть свойство параметра Обновления собрания</span><span class="sxs-lookup"><span data-stu-id="fa7f6-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="fa7f6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa7f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa7f6-105">Скрывает возможность отправки обновлений собраний только добавленным или удаленным участникам.</span><span class="sxs-lookup"><span data-stu-id="fa7f6-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fa7f6-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fa7f6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa7f6-107">Выставлено на:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="fa7f6-108">[Объект IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="fa7f6-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="fa7f6-109">Создано:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-109">Created by:</span></span>  <br/> |<span data-ttu-id="fa7f6-110">Поставщик магазинов</span><span class="sxs-lookup"><span data-stu-id="fa7f6-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="fa7f6-111">Доступ к ним:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="fa7f6-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="fa7f6-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="fa7f6-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-113">Property type:</span></span>  <br/> |<span data-ttu-id="fa7f6-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fa7f6-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fa7f6-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-115">Access type:</span></span>  <br/> |<span data-ttu-id="fa7f6-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fa7f6-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa7f6-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa7f6-117">Remarks</span></span>

<span data-ttu-id="fa7f6-118">Чтобы обеспечить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданных [вызову IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="fa7f6-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="fa7f6-119">Когда тег свойства для любого из этих свойств передается [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="fa7f6-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="fa7f6-120">Поставщики магазинов могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или установить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="fa7f6-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="fa7f6-121">Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="fa7f6-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="fa7f6-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames:_</span><span class="sxs-lookup"><span data-stu-id="fa7f6-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa7f6-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="fa7f6-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="fa7f6-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="fa7f6-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-125">ulKind:</span></span>  <br/> |<span data-ttu-id="fa7f6-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="fa7f6-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="fa7f6-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="fa7f6-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="fa7f6-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="fa7f6-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="fa7f6-129">Поставщик магазина, использующий сервер для отправки обновлений собраний, может изменить диалоговое окно Отправка обновления **участникам.**</span><span class="sxs-lookup"><span data-stu-id="fa7f6-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="fa7f6-130">Эта функция полезна, так как при отправке обновления собрания сервер не знает, какие участники были добавлены или удалены пользователем после первоначального запроса собрания.</span><span class="sxs-lookup"><span data-stu-id="fa7f6-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="fa7f6-131">Если это свойство **верно,** обновление **Отправка** только для добавленных или удаленных участников не отображается в диалоговом окне **Отправка** обновления участникам.</span><span class="sxs-lookup"><span data-stu-id="fa7f6-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="fa7f6-132">Это свойство игнорируется, если версия Outlook более ранней Microsoft Office Outlook 2003 Пакет обновления 1, или если его значение является **ложным.**</span><span class="sxs-lookup"><span data-stu-id="fa7f6-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

