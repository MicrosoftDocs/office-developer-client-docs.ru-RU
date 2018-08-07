---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Возвращает отображаемое имя учетной записи, доставить сообщение.
ms.openlocfilehash: 223bc5bbd485426676376d94875274613ff59685
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807939"
---
# <a name="pidlidinternetaccountname"></a><span data-ttu-id="0bc33-103">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="0bc33-103">PidLidInternetAccountName</span></span>

<span data-ttu-id="0bc33-104">Возвращает отображаемое имя учетной записи, доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="0bc33-104">Returns the display name of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0bc33-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="0bc33-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bc33-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0bc33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0bc33-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="0bc33-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="0bc33-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0bc33-108">Property set:</span></span>  <br/> |<span data-ttu-id="0bc33-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0bc33-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0bc33-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0bc33-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0bc33-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="0bc33-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="0bc33-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0bc33-112">Data type:</span></span>  <br/> |<span data-ttu-id="0bc33-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0bc33-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0bc33-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0bc33-114">Area:</span></span>  <br/> |<span data-ttu-id="0bc33-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="0bc33-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bc33-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0bc33-116">Remarks</span></span>

<span data-ttu-id="0bc33-117">Это свойство должно содержать такое же значение, которое возвращается из API управления учетными данными свойство [PROP_ACCT_NAME](prop_acct_name.md) для учетной записи, которые доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="0bc33-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_NAME](prop_acct_name.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="0bc33-118">Поставщики хранилища сообщений предоставляют доступ к этой именованное свойство и [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) , чтобы выполняются перечисленные ниже действия:</span><span class="sxs-lookup"><span data-stu-id="0bc33-118">Message store providers expose this named property and [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="0bc33-119">Когда пользователь щелкает **Ответить всем** в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью и отметка на сообщение из списка получателей ответа.</span><span class="sxs-lookup"><span data-stu-id="0bc33-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="0bc33-120">Эта проблема возникает, если этот адрес электронной почты отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="0bc33-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="0bc33-121">По умолчанию Outlook отправляет ответов и пересылки сообщений через учетную запись, записывается исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="0bc33-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="0bc33-122">Как правило диспетчер протокола Outlook доставляет сообщения и Outlook задает свойств **PidLidInternetAccountName** и **PidLidInternetAccountStamp** , чтобы указать учетную запись, доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="0bc33-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="0bc33-123">Тем не менее если хранилища сообщений тесно связан с транспорта, диспетчер протокола Outlook не доставлять сообщения и Outlook не удается задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="0bc33-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="0bc33-124">В этом сценарии Outlook вызывает функцию [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0bc33-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="0bc33-125">Если поставщик хранения сообщений хочет эти именованные свойства, следует реализовать **IMAPIProp::GetIDsFromNames** и возврата теги свойства через параметр вывода *lppPropTags* .</span><span class="sxs-lookup"><span data-stu-id="0bc33-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="0bc33-126">Outlook может затем вызвать метод [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) с помощью этих свойств теги и поставщика хранилища сообщений можно вернуть имя учетной записи и метка нужную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0bc33-126">Outlook can then call the [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="0bc33-127">Чтобы обеспечить поддержку этих именованных свойств, поставщиков хранилища следует ожидать Outlook использование **IMAPIProp::GetIDsFromNames** для получения тег свойства для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="0bc33-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="0bc33-128">Outlook задает следующие значения для структуры [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) , соответствующий этой именованного свойства, который передается как часть массива, на которую указывает входного параметра *lppPropNames* из **IMAPIProp::GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="0bc33-128">Outlook specifies the following values for the [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bc33-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="0bc33-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="0bc33-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0bc33-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0bc33-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="0bc33-131">ulKind:</span></span>  <br/> |<span data-ttu-id="0bc33-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="0bc33-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="0bc33-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="0bc33-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="0bc33-134">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="0bc33-134">dispidInetAcctName</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0bc33-135">См. также</span><span class="sxs-lookup"><span data-stu-id="0bc33-135">See also</span></span>

- [<span data-ttu-id="0bc33-136">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="0bc33-136">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="0bc33-137">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="0bc33-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="0bc33-138">Каноническое свойство PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="0bc33-138">PidLidInternetAccountName Canonical Property</span></span>](http://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

