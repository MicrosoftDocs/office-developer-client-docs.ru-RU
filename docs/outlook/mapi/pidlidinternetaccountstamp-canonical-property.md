---
title: Каноническое свойство PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 49732f30461e05e83c130f9cc24129cc86baa75f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810390"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="0d801-103">Каноническое свойство PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="0d801-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="0d801-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d801-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d801-105">Задает идентификатор учетной записи электронной почты, через который отправляется сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0d801-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d801-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0d801-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d801-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="0d801-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="0d801-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0d801-108">Property set:</span></span>  <br/> |<span data-ttu-id="0d801-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0d801-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0d801-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0d801-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0d801-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="0d801-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="0d801-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0d801-112">Data type:</span></span>  <br/> |<span data-ttu-id="0d801-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d801-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0d801-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0d801-114">Area:</span></span>  <br/> |<span data-ttu-id="0d801-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="0d801-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d801-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0d801-116">Remarks</span></span>

<span data-ttu-id="0d801-117">Формат этой строки — зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="0d801-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="0d801-118">Это свойство можно использовать клиента, чтобы определить, какой сервер для направления почтовое приложение должно, но является необязательным, и значение не имеет значения для сервера.</span><span class="sxs-lookup"><span data-stu-id="0d801-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d801-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0d801-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d801-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0d801-120">Protocol specifications</span></span>

<span data-ttu-id="0d801-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d801-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d801-122">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0d801-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d801-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d801-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d801-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0d801-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d801-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0d801-125">Header files</span></span>

<span data-ttu-id="0d801-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d801-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d801-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0d801-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d801-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0d801-128">See also</span></span>



[<span data-ttu-id="0d801-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0d801-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d801-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0d801-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d801-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0d801-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d801-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0d801-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

