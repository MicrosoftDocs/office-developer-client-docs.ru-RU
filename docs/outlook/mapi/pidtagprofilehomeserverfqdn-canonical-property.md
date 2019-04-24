---
title: Каноническое свойство PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341596"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="b105f-103">Каноническое свойство PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="b105f-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="b105f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b105f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b105f-105">Включает проверку подлинности Kerberos для конфигурации профиля.</span><span class="sxs-lookup"><span data-stu-id="b105f-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="b105f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b105f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b105f-107">ПР_ПРОФИЛЕ_ХОМЕ_СЕРВЕР_ФКДН</span><span class="sxs-lookup"><span data-stu-id="b105f-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="b105f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b105f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b105f-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="b105f-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="b105f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b105f-110">Data type:</span></span>  <br/> |<span data-ttu-id="b105f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b105f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b105f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b105f-112">Area:</span></span>  <br/> |<span data-ttu-id="b105f-113">Конфигурация профиля MAPI</span><span class="sxs-lookup"><span data-stu-id="b105f-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b105f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b105f-114">Remarks</span></span>

<span data-ttu-id="b105f-115">Задание этого свойства для доменного имени сервера каталогов пользователя позволяет напрямую подключиться к контроллеру домена (DC), который необходим для профиля, настроенного для использования проверки подлинности Kerberos в Microsoft Exchange Server 2007 и более ранние версии, устанавливая **рпк_к_аусн_гсс_керберос** в **пр_профиле_аус_паккаже**.</span><span class="sxs-lookup"><span data-stu-id="b105f-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b105f-116">Microsoft Exchange Server 2010 и Exchange Server 2013 обрабатывают вызовы адресных книг, выполняемые на сервере клиентского доступа, так же, как Exchange Server 2007 и более ранние версии обрабатывают их.</span><span class="sxs-lookup"><span data-stu-id="b105f-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="b105f-117">Процесс DSProxy больше не используется, поэтому проверка подлинности Kerberos может быть успешной.</span><span class="sxs-lookup"><span data-stu-id="b105f-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="b105f-118">Однако клиент по-прежнему будет взаимодействовать с сервером Exchange Server, а не с КОНТРОЛЛЕРом домена, что может быть нежелательным. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b105f-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b105f-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b105f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b105f-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b105f-120">Protocol specifications</span></span>

<span data-ttu-id="b105f-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b105f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b105f-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b105f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b105f-123">[[MS — ОКСКСТОР]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b105f-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b105f-124">Указывает допустимые операции для основных объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b105f-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b105f-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b105f-125">Header files</span></span>

<span data-ttu-id="b105f-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b105f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b105f-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b105f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b105f-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b105f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b105f-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b105f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b105f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b105f-130">See also</span></span>



[<span data-ttu-id="b105f-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b105f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b105f-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b105f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b105f-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b105f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b105f-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b105f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

