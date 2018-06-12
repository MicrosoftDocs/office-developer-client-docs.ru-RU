---
title: Скрыть свойство параметр обновление собрания
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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808584"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="037e7-103">Скрыть свойство параметр обновление собрания</span><span class="sxs-lookup"><span data-stu-id="037e7-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="037e7-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="037e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="037e7-105">Скрывает отправка обновлений встреч только добавленным или удаленным участникам.</span><span class="sxs-lookup"><span data-stu-id="037e7-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="037e7-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="037e7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="037e7-107">Предоставляется для:</span><span class="sxs-lookup"><span data-stu-id="037e7-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="037e7-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект</span><span class="sxs-lookup"><span data-stu-id="037e7-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="037e7-109">Созданные:</span><span class="sxs-lookup"><span data-stu-id="037e7-109">Created by:</span></span>  <br/> |<span data-ttu-id="037e7-110">Поставщик хранения</span><span class="sxs-lookup"><span data-stu-id="037e7-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="037e7-111">Чтобы открыть:</span><span class="sxs-lookup"><span data-stu-id="037e7-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="037e7-112">Outlook и другие клиенты</span><span class="sxs-lookup"><span data-stu-id="037e7-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="037e7-113">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="037e7-113">Property type:</span></span>  <br/> |<span data-ttu-id="037e7-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="037e7-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="037e7-115">Тип доступа:</span><span class="sxs-lookup"><span data-stu-id="037e7-115">Access type:</span></span>  <br/> |<span data-ttu-id="037e7-116">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="037e7-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="037e7-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="037e7-117">Remarks</span></span>

<span data-ttu-id="037e7-118">Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="037e7-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="037e7-119">При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство.</span><span class="sxs-lookup"><span data-stu-id="037e7-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="037e7-120">Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="037e7-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="037e7-121">Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="037e7-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="037e7-122">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="037e7-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="037e7-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="037e7-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="037e7-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="037e7-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="037e7-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="037e7-125">ulKind:</span></span>  <br/> |<span data-ttu-id="037e7-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="037e7-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="037e7-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="037e7-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="037e7-128">L "urn: schemas-microsoft-com:office:outlook #allornonemtgupdatedlg»</span><span class="sxs-lookup"><span data-stu-id="037e7-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="037e7-129">Поставщик хранилища, которое использует сервер для отправки обновлений встреч можно изменить диалоговое окно **Отправить обновление участникам** .</span><span class="sxs-lookup"><span data-stu-id="037e7-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="037e7-130">Эта функция полезна, так как при сервер отправляет обновление собрания, сервер не знаете, какие участники были добавлены или удалены пользователем, начиная с начального приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="037e7-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="037e7-131">Если это свойство имеет **значение true**, параметр **Отправить обновления только добавленным или удаленным участникам** не отображается в диалоговом окне **Отправить обновление участникам** .</span><span class="sxs-lookup"><span data-stu-id="037e7-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="037e7-132">Это свойство игнорируется, если используется Outlook версии более ранней, чем пакет обновления 1 для Microsoft Office Outlook 2003 или имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="037e7-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

