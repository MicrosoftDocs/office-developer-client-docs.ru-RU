---
title: Каноническое свойство PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3c90284671d6087c74d4541b1a4774cc13b3ada5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583192"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="8589e-103">Каноническое свойство PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="8589e-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="8589e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8589e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8589e-105">Содержит динамически созданных GUID используется для определения учетной записи при использовании нескольких учетных записей сервера Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="8589e-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8589e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8589e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8589e-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="8589e-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="8589e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8589e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8589e-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="8589e-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="8589e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8589e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8589e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8589e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8589e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8589e-112">Area:</span></span>  <br/> |<span data-ttu-id="8589e-113">Несколько учетных записей Exchange</span><span class="sxs-lookup"><span data-stu-id="8589e-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8589e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8589e-114">Remarks</span></span>

<span data-ttu-id="8589e-115">Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживает несколько учетных записей Exchange вместо одной одной учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="8589e-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="8589e-116">Чтобы обеспечить несколько учетных записей Exchange, макет профилей MAPI был изменен.</span><span class="sxs-lookup"><span data-stu-id="8589e-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="8589e-117">В Microsoft Office Outlook 2007 и более ранних версий профили содержащиеся раздела основных профиля, выделенного для параметров Exchange, такие как имя сервера, имя пользователя и файла автономной папки (OST).</span><span class="sxs-lookup"><span data-stu-id="8589e-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="8589e-118">расположение.</span><span class="sxs-lookup"><span data-stu-id="8589e-118">location.</span></span> <span data-ttu-id="8589e-119">Эти параметры обнаружены с помощью уникального идентификатора, свойство **pbGlobalProfileSectionGuid** .</span><span class="sxs-lookup"><span data-stu-id="8589e-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="8589e-120">Раздел, используемый для параметров Exchange называется глобального раздела профиля Exchange.</span><span class="sxs-lookup"><span data-stu-id="8589e-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> <span data-ttu-id="8589e-121">Дополнительные сведения о глобальных профиля Exchange в Outlook 2007 [как открыть общий раздел профилей](http://support.microsoft.com/kb/188482)см.</span><span class="sxs-lookup"><span data-stu-id="8589e-121">For more information about the Exchange Global Profile in Outlook 2007, see [How To Open the Global Profile Section](http://support.microsoft.com/kb/188482).</span></span>
  
<span data-ttu-id="8589e-122">Расположение раздела основных профиля больше не достаточно для учета нескольких учетных записей Exchange.</span><span class="sxs-lookup"><span data-stu-id="8589e-122">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="8589e-123">Вместо этого для каждой учетной записи Exchange в профиле раздел существует, предназначенный для параметров для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8589e-123">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="8589e-124">Уникальный идентификатор **emsmdbUID**определяется новый раздел, используемые для параметров Exchange.</span><span class="sxs-lookup"><span data-stu-id="8589e-124">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="8589e-125">В разделе профиля службы сообщений для учетной записи Exchange можно найти свойство, которое содержит идентификатор GUID, создаваемый динамически во время создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8589e-125">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="8589e-126">Идентификатор GUID хранится в свойстве **PidTagExchangeProfileSectionId** .</span><span class="sxs-lookup"><span data-stu-id="8589e-126">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="8589e-127">Хранилищ сообщений и адресной книги контейнеры предоставляют свойство так, чтобы определить, какая учетная запись Exchange, он входит.</span><span class="sxs-lookup"><span data-stu-id="8589e-127">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="8589e-128">Доступно в таблице служб сообщения, это свойство предоставляет каждой службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="8589e-128">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="8589e-129">Это свойство посредством вызова [IMAPIProp::GetProps](imapiprop-getprops.md) на **PidTagExchangeProfileSectionId** можно получить после запроса для каких-либо следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="8589e-129">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="8589e-130">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8589e-130">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="8589e-131">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8589e-131">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="8589e-132">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8589e-132">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="8589e-133">Если объект не связан с сервером Exchange, вызов возвращает **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="8589e-133">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="8589e-134">Можно ограничить контейнеров в **PidTagExchangeProfileSectionId** при отображении в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="8589e-134">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="8589e-135">При наличии открытых контейнер, можно выполнить запрос **emsmdbUID** из нее.</span><span class="sxs-lookup"><span data-stu-id="8589e-135">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="8589e-136">Это также следует отметить, что если получатель была выбрана в адресной книге Exchange, у получателя также установлена **PidTagExchangeProfileSectionId** в списке свойств.</span><span class="sxs-lookup"><span data-stu-id="8589e-136">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8589e-137">Идентификатор GUID во всей функции заголовки и примеры кода, называется **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="8589e-137">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="8589e-138">Один из учетных записей Exchange отмечен как устаревшие учетные записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="8589e-138">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="8589e-139">Как правило это первую учетную запись, добавляемого к профилю.</span><span class="sxs-lookup"><span data-stu-id="8589e-139">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="8589e-140">Каждого вызова, чтобы открыть **pbGlobalProfileSectionGuid** перенаправляется в глобальный раздел Exchange прежней версии.</span><span class="sxs-lookup"><span data-stu-id="8589e-140">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="8589e-141">Вызовы объектной модели, которые взаимодействуют с учетной записью Exchange не прежних версий также взаимодействовать с учетной записью Exchange прежних версий.</span><span class="sxs-lookup"><span data-stu-id="8589e-141">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="8589e-142">Служба Exchange прежних версий имеет свойство **PR_EMSMDB_LEGACY** (0x3D18000B) которого имеет значение **true** в таблице служб сообщения.</span><span class="sxs-lookup"><span data-stu-id="8589e-142">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="8589e-143">Прежних версий **emsmdbUID** также записывается в раздел глобальный профиль Outlook профиля как **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="8589e-143">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="8589e-144">Код, написанный для поддержки нескольких учетных записей Exchange для получения прежних версий **emsmdbUID** , так как он должны получить правильные **emsmdbUID**, в зависимости от того, с учетной записью, взаимодействует код не должен.</span><span class="sxs-lookup"><span data-stu-id="8589e-144">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8589e-145">См. также</span><span class="sxs-lookup"><span data-stu-id="8589e-145">See also</span></span>



[<span data-ttu-id="8589e-146">Использование нескольких учетных записей Exchange</span><span class="sxs-lookup"><span data-stu-id="8589e-146">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="8589e-147">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="8589e-147">How To Open the Global Profile Section</span></span>](http://support.microsoft.com/kb/188482)

