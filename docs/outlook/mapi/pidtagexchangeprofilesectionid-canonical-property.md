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
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316431"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="9f59a-103">Каноническое свойство PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="9f59a-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="9f59a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f59a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f59a-105">Содержит динамически генерируемый GUID, используемый для определения учетной записи при использовании нескольких Microsoft Exchange Server учетных записей.</span><span class="sxs-lookup"><span data-stu-id="9f59a-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f59a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9f59a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f59a-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="9f59a-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="9f59a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9f59a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f59a-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="9f59a-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="9f59a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9f59a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f59a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9f59a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9f59a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9f59a-112">Area:</span></span>  <br/> |<span data-ttu-id="9f59a-113">Несколько учетных записей Exchange</span><span class="sxs-lookup"><span data-stu-id="9f59a-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f59a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9f59a-114">Remarks</span></span>

<span data-ttu-id="9f59a-115">Microsoft Outlook 2010, русская версия Microsoft Outlook 2013 поддерживают несколько учетных записей Exchange вместо одной учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="9f59a-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="9f59a-116">Для размещения нескольких учетных записей Exchange макет профиля MAPI был изменен.</span><span class="sxs-lookup"><span data-stu-id="9f59a-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="9f59a-117">В Microsoft Office Outlook 2007 и более ранних, профили содержали фиксированный раздел профиля, выделенный для параметров Exchange, таких как имя сервера, имя пользователя и файл автономной папки (OST).</span><span class="sxs-lookup"><span data-stu-id="9f59a-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="9f59a-118">расположение.</span><span class="sxs-lookup"><span data-stu-id="9f59a-118">location.</span></span> <span data-ttu-id="9f59a-119">Эти параметры были определены с помощью уникального идентификатора, **свойства pbGlobalProfileSectionGuid.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="9f59a-120">Раздел, используемый для параметров Exchange, называется разделом глобального профиля Exchange.</span><span class="sxs-lookup"><span data-stu-id="9f59a-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="9f59a-121">Фиксированного расположения раздела профиля больше недостаточно для размещения нескольких учетных записей Exchange.</span><span class="sxs-lookup"><span data-stu-id="9f59a-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="9f59a-122">Вместо этого для каждой учетной записи Exchange в профиле существует раздел, выделенный для параметров этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9f59a-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="9f59a-123">Новый раздел, используемый для параметров Exchange, определяется уникальным идентификатором **emsmdbUID.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="9f59a-124">В разделе профиля службы сообщений для учетной записи Exchange можно найти свойство, которое содержит GUID, динамически генерируемый во время создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9f59a-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="9f59a-125">Этот GUID хранится в свойстве **PidTagExchangeProfileSectionId.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="9f59a-126">Хранилища сообщений и контейнеры адресной книги предоставляет свойство, определяя, к какой учетной записи Exchange они принадлежат.</span><span class="sxs-lookup"><span data-stu-id="9f59a-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="9f59a-127">Доступно в таблице служб сообщений, каждая служба Exchange предоставляет это свойство.</span><span class="sxs-lookup"><span data-stu-id="9f59a-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="9f59a-128">Это свойство можно получить с помощью вызова [IMAPIProp::GetProps](imapiprop-getprops.md) на **pidTagExchangeProfileSectionId** после запроса любого из следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="9f59a-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="9f59a-129">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9f59a-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="9f59a-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9f59a-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="9f59a-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9f59a-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="9f59a-132">Если объект не связан с Exchange, вызов возвращает **MAPI_E_NOT_FOUND.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="9f59a-133">При отображении адресной книги можно ограничить контейнеры **для PidTagExchangeProfileSectionId.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="9f59a-134">После открытия контейнера можно запросить у **него emsmdbUID.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="9f59a-135">Также стоит отметить, что если получатель был выбран из адресной книги Exchange, в списке свойств получателя также есть **pidTagExchangeProfileSectionId.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9f59a-136">Во всех примерах кода и в заголовщиках функций этот GUID называется **emsmdbUID.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="9f59a-137">Одна из учетных записей Exchange помечена как устаревшая учетная запись Exchange.</span><span class="sxs-lookup"><span data-stu-id="9f59a-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="9f59a-138">Обычно это первая учетная запись, добавленная в профиль.</span><span class="sxs-lookup"><span data-stu-id="9f59a-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="9f59a-139">Каждый вызов для открытия **pbGlobalProfileSectionGuid** перенаправляется в глобальный раздел Exchange устаревшей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9f59a-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="9f59a-140">Вызовы объектной модели, взаимодействующие с устаревшей учетной записью Exchange, также взаимодействуют с устаревшей учетной записью Exchange.</span><span class="sxs-lookup"><span data-stu-id="9f59a-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="9f59a-141">Устаревшая служба Exchange имеет свойство **PR_EMSMDB_LEGACY** (0x3D18000B), которое имеет true **в** таблице служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f59a-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="9f59a-142">**Устаревшее emsmdbUID** также помещается в разделе глобального профиля Outlook профиля как **PidTagExchangeProfileSectionId.**</span><span class="sxs-lookup"><span data-stu-id="9f59a-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="9f59a-143">Код, написанный для поддержки нескольких учетных записей Exchange, не должен извлекать устаревший **emsmdbUID,** так как он должен получать правильный **emsmdbUID** в зависимости от учетной записи, с помощью которых взаимодействует код.</span><span class="sxs-lookup"><span data-stu-id="9f59a-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f59a-144">См. также</span><span class="sxs-lookup"><span data-stu-id="9f59a-144">See also</span></span>



[<span data-ttu-id="9f59a-145">Использование нескольких учетных записей Exchange</span><span class="sxs-lookup"><span data-stu-id="9f59a-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="9f59a-146">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="9f59a-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

