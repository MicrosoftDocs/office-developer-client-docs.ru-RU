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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400357"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="1f7dc-103">Каноническое свойство PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="1f7dc-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="1f7dc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f7dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f7dc-105">Включение проверки подлинности Kerberos для настройки профилей.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="1f7dc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1f7dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f7dc-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="1f7dc-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="1f7dc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1f7dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f7dc-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="1f7dc-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="1f7dc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1f7dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f7dc-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f7dc-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1f7dc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1f7dc-112">Area:</span></span>  <br/> |<span data-ttu-id="1f7dc-113">Настройки профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="1f7dc-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f7dc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f7dc-114">Remarks</span></span>

<span data-ttu-id="1f7dc-115">Установка для этого свойства доменное имя сервера каталогов пользователя позволяет прямое подключение к домена Контроллера, который требуется для профиля, который был настроен для использования проверки подлинности Kerberos с Microsoft Exchange Server 2007 и более ранних версий, задав **RPC_C_AUTHN_GSS_KERBEROS** в **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1f7dc-116">Microsoft Exchange Server 2010 и Exchange Server 2013 обрабатывать адресной книги вызовах на сервер клиентского доступа по-разному от того, в котором сервер Exchange Server 2007 и более ранних версий их обработки.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="1f7dc-117">Процесс DSProxy больше не используется, поэтому может завершиться без ошибок проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="1f7dc-118">Тем не менее, клиент будет по-прежнему связи с Exchange server, а не непосредственно с контроллера домена, который не может потребоваться: параметр позволяет избежать **PR_PROFILE_HOME_SERVER_FQDN** это.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f7dc-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1f7dc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f7dc-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1f7dc-120">Protocol specifications</span></span>

<span data-ttu-id="1f7dc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f7dc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f7dc-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f7dc-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f7dc-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f7dc-124">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f7dc-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1f7dc-125">Header files</span></span>

<span data-ttu-id="1f7dc-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f7dc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f7dc-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f7dc-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f7dc-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1f7dc-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1f7dc-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f7dc-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1f7dc-130">See also</span></span>



[<span data-ttu-id="1f7dc-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f7dc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f7dc-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f7dc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f7dc-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1f7dc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f7dc-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1f7dc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

