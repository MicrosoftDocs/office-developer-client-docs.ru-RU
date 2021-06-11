---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Возвращает отпечаток учетной записи учетной записи, которая доставляла сообщение.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327729"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="a8aec-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="a8aec-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="a8aec-104">Возвращает отпечаток учетной записи учетной записи, которая доставляла сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8aec-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8aec-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a8aec-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8aec-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a8aec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8aec-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="a8aec-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="a8aec-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a8aec-108">Property set:</span></span>  <br/> |<span data-ttu-id="a8aec-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a8aec-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a8aec-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a8aec-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a8aec-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="a8aec-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="a8aec-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a8aec-112">Data type:</span></span>  <br/> |<span data-ttu-id="a8aec-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a8aec-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a8aec-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a8aec-114">Area:</span></span>  <br/> |<span data-ttu-id="a8aec-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="a8aec-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8aec-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8aec-116">Remarks</span></span>

<span data-ttu-id="a8aec-117">Это свойство должно содержать то же значение, которое возвращается из свойства API [управления](prop_acct_stamp.md) учетной записью PROP_ACCT_STAMP для учетной записи, доставляемой сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8aec-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="a8aec-118">Поставщики магазинов сообщений раскрывают это свойство с именем [PidLidInternetAccountName,](pidlidinternetaccountname.md) чтобы произошло следующее:</span><span class="sxs-lookup"><span data-stu-id="a8aec-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="a8aec-119">Когда пользователь нажимает кнопку Ответ на все в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью и штампуется в сообщении из списка получателей ответа. </span><span class="sxs-lookup"><span data-stu-id="a8aec-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="a8aec-120">Такое поведение происходит, если этот адрес электронной почты не является отправивлю исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8aec-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="a8aec-121">По умолчанию Outlook отправляет ответы и отправляет сообщения через учетную запись, штампуемую в исходном сообщении.</span><span class="sxs-lookup"><span data-stu-id="a8aec-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="a8aec-122">Обычно диспетчер Outlook протоколов доставляет сообщения, а Outlook задает свойства **PidLidInternetAccountName** и **PidLidInternetAccountStamp,** чтобы указать учетную запись, которая передала сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8aec-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="a8aec-123">Однако если хранилище сообщений тесно совмещение с транспортом, диспетчер протокола Outlook не доставляет сообщения, и Outlook не может задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a8aec-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="a8aec-124">В этом сценарии Outlook [вызывает функцию IMAPIProp::GetIDsFromNames.](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8aec-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="a8aec-125">Если поставщик магазина сообщений хочет раскрыть эти свойства, он должен реализовать **IMAPIProp::GetIDsFromNames** и вернуть теги свойств через параметр  *вывода lppPropTags*  .</span><span class="sxs-lookup"><span data-stu-id="a8aec-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="a8aec-126">Outlook затем можно вызвать метод [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) с помощью этих тегов свойств, а поставщик магазина сообщений может вернуть имя учетной записи и печать нужной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a8aec-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="a8aec-127">Чтобы поддерживать указанные свойства, поставщики магазинов должны ожидать, что Outlook использовать **IMAPIProp::GetIDsFromNames** для получения тега свойства для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a8aec-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="a8aec-128">Outlook указывает следующие значения для структуры [MAPINAMEID,](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) соответствующей этому имени свойства, которое передается как часть массива, указанного в параметре *ввода lppPropNames* **IMAPIProp::GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="a8aec-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8aec-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="a8aec-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="a8aec-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a8aec-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a8aec-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="a8aec-131">ulKind:</span></span>  <br/> |<span data-ttu-id="a8aec-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="a8aec-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="a8aec-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="a8aec-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="a8aec-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="a8aec-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8aec-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a8aec-135">See also</span></span>

- [<span data-ttu-id="a8aec-136">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="a8aec-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="a8aec-137">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="a8aec-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="a8aec-138">Каноническое свойство PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="a8aec-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

