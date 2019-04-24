---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Возвращает отображаемое имя учетной записи, которая доставила сообщение.
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327687"
---
# <a name="pidlidinternetaccountname"></a><span data-ttu-id="9d3e9-103">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="9d3e9-103">PidLidInternetAccountName</span></span>

<span data-ttu-id="9d3e9-104">Возвращает отображаемое имя учетной записи, которая доставила сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-104">Returns the display name of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9d3e9-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9d3e9-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d3e9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d3e9-107">Диспидинетакктнаме</span><span class="sxs-lookup"><span data-stu-id="9d3e9-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="9d3e9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-108">Property set:</span></span>  <br/> |<span data-ttu-id="9d3e9-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="9d3e9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9d3e9-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="9d3e9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9d3e9-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="9d3e9-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="9d3e9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-112">Data type:</span></span>  <br/> |<span data-ttu-id="9d3e9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9d3e9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9d3e9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-114">Area:</span></span>  <br/> |<span data-ttu-id="9d3e9-115">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="9d3e9-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d3e9-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="9d3e9-116">Remarks</span></span>

<span data-ttu-id="9d3e9-117">Это свойство должно содержать то же значение, которое возвращается из свойства API управления учетными записями [проп_аккт_наме](prop_acct_name.md) для учетной записи, которая доставила сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_NAME](prop_acct_name.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="9d3e9-118">Поставщики хранилищ сообщений предоставляют это именованное свойство и [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) , поэтому выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-118">Message store providers expose this named property and [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="9d3e9-119">Когда пользователь нажимает кнопку **ответить на все** в сообщении электронной почты, Outlook удаляет адрес электронной почты, связанный с учетной записью, и отмечает сообщение из списка получателей ответа.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="9d3e9-120">Эта проблема возникает, если этот адрес электронной почты является отправителем исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="9d3e9-121">По умолчанию Outlook отправляет ответы и пересылаемые сообщения с помощью учетной записи, помеченной на исходном сообщении.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="9d3e9-122">Как правило, диспетчер протокола Outlook доставляет сообщения, и Outlook устанавливает свойства **PidLidInternetAccountName** и **PidLidInternetAccountStamp** , чтобы указать учетную запись, которая доставила сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="9d3e9-123">Однако если банк сообщений тесно связан с транспортом, Диспетчер протоколов Outlook не Додает сообщения и Outlook не может задать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="9d3e9-124">В этом сценарии Outlook вызывает функцию [IMAPIProp:: жетидсфромнамес](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9d3e9-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="9d3e9-125">Если поставщик хранилища сообщений хочет предоставить эти именованные свойства, он должен реализовать **IMAPIProp:: жетидсфромнамес** и возвращать теги свойств через выходной параметр *лпппроптагс* .</span><span class="sxs-lookup"><span data-stu-id="9d3e9-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="9d3e9-126">Затем в Outlook можно вызвать метод [IMAPIProp::](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) GetProperty с помощью этих тегов свойств, а поставщик хранилища сообщений может вернуть имя и метку учетной записи нужной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="9d3e9-127">Для поддержки этих именованных свойств поставщики хранилища должны ожидать, что Outlook будет использовать **IMAPIProp:: жетидсфромнамес** , чтобы получить тег свойства для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="9d3e9-128">Outlook задает следующие значения для структуры [мапинамеид](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) , которая соответствует этому именованному свойству, которое передается как часть массива, на который указывает входный параметр *лпппропнамес* **IMAPIProp:: жетидсфромнамес**.</span><span class="sxs-lookup"><span data-stu-id="9d3e9-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d3e9-129">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="9d3e9-130">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="9d3e9-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9d3e9-131">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-131">ulKind:</span></span>  <br/> |<span data-ttu-id="9d3e9-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="9d3e9-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="9d3e9-133">Вид: крышка:</span><span class="sxs-lookup"><span data-stu-id="9d3e9-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="9d3e9-134">Диспидинетакктнаме</span><span class="sxs-lookup"><span data-stu-id="9d3e9-134">dispidInetAcctName</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d3e9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9d3e9-135">See also</span></span>

- [<span data-ttu-id="9d3e9-136">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="9d3e9-136">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="9d3e9-137">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="9d3e9-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="9d3e9-138">Каноническое свойство PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="9d3e9-138">PidLidInternetAccountName Canonical Property</span></span>](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

