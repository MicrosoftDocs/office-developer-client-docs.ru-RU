---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Возвращает метку учетной записи, которая доставила сообщение.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327729"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="caa09-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="caa09-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="caa09-104">Возвращает метку учетной записи, которая доставила сообщение.</span><span class="sxs-lookup"><span data-stu-id="caa09-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="caa09-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="caa09-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="caa09-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="caa09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="caa09-107">Диспидинетакктстамп</span><span class="sxs-lookup"><span data-stu-id="caa09-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="caa09-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="caa09-108">Property set:</span></span>  <br/> |<span data-ttu-id="caa09-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="caa09-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="caa09-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="caa09-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="caa09-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="caa09-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="caa09-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="caa09-112">Data type:</span></span>  <br/> |<span data-ttu-id="caa09-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="caa09-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="caa09-114">Область:</span><span class="sxs-lookup"><span data-stu-id="caa09-114">Area:</span></span>  <br/> |<span data-ttu-id="caa09-115">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="caa09-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="caa09-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="caa09-116">Remarks</span></span>

<span data-ttu-id="caa09-117">Это свойство должно содержать то же значение, которое возвращается из свойства API управления учетными записями [проп_аккт_стамп](prop_acct_stamp.md) для учетной записи, которая доставила сообщение.</span><span class="sxs-lookup"><span data-stu-id="caa09-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="caa09-118">Поставщики хранилищ сообщений предоставляют это именованное свойство и [PidLidInternetAccountName](pidlidinternetaccountname.md) , поэтому выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="caa09-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="caa09-119">Когда пользователь нажимает кнопку **ответить на все** в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью, и отмечает сообщение из списка получателей ответа.</span><span class="sxs-lookup"><span data-stu-id="caa09-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="caa09-120">Эта проблема возникает, если этот адрес электронной почты является отправителем исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="caa09-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="caa09-121">По умолчанию Outlook отправляет ответы и пересылаемые сообщения с помощью учетной записи, помеченной на исходном сообщении.</span><span class="sxs-lookup"><span data-stu-id="caa09-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="caa09-122">Как правило, диспетчер протокола Outlook доставляет сообщения, и Outlook устанавливает свойства **PidLidInternetAccountName** и **PidLidInternetAccountStamp** , чтобы указать учетную запись, которая доставила сообщение.</span><span class="sxs-lookup"><span data-stu-id="caa09-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="caa09-123">Однако если банк сообщений тесно связан с транспортом, Диспетчер протоколов Outlook не Додает сообщения и Outlook не может задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="caa09-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="caa09-124">В этом сценарии Outlook вызывает функцию [IMAPIProp:: жетидсфромнамес](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="caa09-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="caa09-125">Если поставщик хранилища сообщений хочет предоставить эти именованные свойства, он должен реализовать **IMAPIProp:: жетидсфромнамес** и возвращать теги свойств через выходной параметр *лпппроптагс* .</span><span class="sxs-lookup"><span data-stu-id="caa09-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="caa09-126">Затем в Outlook можно вызвать метод [IMAPIProp::](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) GetProperty с помощью этих тегов свойств, а поставщик хранилища сообщений может вернуть имя и метку учетной записи нужной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="caa09-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="caa09-127">Для поддержки этих именованных свойств поставщики хранилища должны ожидать, что Outlook будет использовать **IMAPIProp:: жетидсфромнамес** , чтобы получить тег свойства для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="caa09-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="caa09-128">Outlook задает следующие значения для структуры [мапинамеид](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) , которая соответствует этому именованному свойству, которое передается как часть массива, на который указывает входный параметр *лпппропнамес* **IMAPIProp:: жетидсфромнамес**.</span><span class="sxs-lookup"><span data-stu-id="caa09-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="caa09-129">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="caa09-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="caa09-130">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="caa09-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="caa09-131">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="caa09-131">ulKind:</span></span>  <br/> |<span data-ttu-id="caa09-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="caa09-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="caa09-133">Вид: крышка:</span><span class="sxs-lookup"><span data-stu-id="caa09-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="caa09-134">Диспидинетакктстамп</span><span class="sxs-lookup"><span data-stu-id="caa09-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="caa09-135">См. также</span><span class="sxs-lookup"><span data-stu-id="caa09-135">See also</span></span>

- [<span data-ttu-id="caa09-136">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="caa09-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="caa09-137">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="caa09-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="caa09-138">Каноническое свойство PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="caa09-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

