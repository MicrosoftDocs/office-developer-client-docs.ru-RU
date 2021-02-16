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
ms.openlocfilehash: ebd64392d24cd170a7babf77865aa00c7be24802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315458"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="f45eb-103">Каноническое свойство PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="f45eb-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="f45eb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f45eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f45eb-105">Указывает ИД учетной записи электронной почты, через которую отправляется сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f45eb-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f45eb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f45eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f45eb-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="f45eb-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="f45eb-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f45eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="f45eb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f45eb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f45eb-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="f45eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f45eb-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="f45eb-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="f45eb-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f45eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="f45eb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f45eb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f45eb-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f45eb-114">Area:</span></span>  <br/> |<span data-ttu-id="f45eb-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="f45eb-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f45eb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f45eb-116">Remarks</span></span>

<span data-ttu-id="f45eb-117">Формат этой строки зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="f45eb-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="f45eb-118">Это свойство может использоваться клиентом для определения сервера, на который направляется почта, но является необязательным, а значение не имеет значения для сервера.</span><span class="sxs-lookup"><span data-stu-id="f45eb-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f45eb-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f45eb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f45eb-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f45eb-120">Protocol specifications</span></span>

<span data-ttu-id="f45eb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f45eb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f45eb-122">Предоставляет определение набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="f45eb-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f45eb-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f45eb-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f45eb-124">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f45eb-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f45eb-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f45eb-125">Header files</span></span>

<span data-ttu-id="f45eb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f45eb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f45eb-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f45eb-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f45eb-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f45eb-128">See also</span></span>



[<span data-ttu-id="f45eb-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f45eb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f45eb-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f45eb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f45eb-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f45eb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f45eb-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f45eb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

