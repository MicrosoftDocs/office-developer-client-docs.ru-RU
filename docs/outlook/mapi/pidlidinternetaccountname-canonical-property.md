---
title: Каноническое свойство PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2da826fe7ab9e4d7ca3eaaf0f9806193c47100d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315493"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="bae60-103">Каноническое свойство PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="bae60-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="bae60-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bae60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bae60-105">Указывает имя учетной записи электронной почты, видимой пользователем, через которую отправляется сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bae60-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bae60-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bae60-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bae60-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="bae60-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="bae60-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="bae60-108">Property set:</span></span>  <br/> |<span data-ttu-id="bae60-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bae60-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bae60-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bae60-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bae60-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="bae60-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="bae60-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bae60-112">Data type:</span></span>  <br/> |<span data-ttu-id="bae60-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bae60-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bae60-114">Область:</span><span class="sxs-lookup"><span data-stu-id="bae60-114">Area:</span></span>  <br/> |<span data-ttu-id="bae60-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="bae60-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bae60-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="bae60-116">Remarks</span></span>

<span data-ttu-id="bae60-117">Формат этой строки зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="bae60-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="bae60-118">Это свойство может быть использовано клиентом для определения сервера, на который направляется почта, но является необязательным и значение не имеет значения для сервера.</span><span class="sxs-lookup"><span data-stu-id="bae60-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bae60-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bae60-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bae60-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bae60-120">Protocol specifications</span></span>

<span data-ttu-id="bae60-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bae60-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bae60-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="bae60-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bae60-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bae60-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bae60-124">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bae60-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bae60-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="bae60-125">Header files</span></span>

<span data-ttu-id="bae60-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bae60-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bae60-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bae60-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bae60-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bae60-128">See also</span></span>



[<span data-ttu-id="bae60-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bae60-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bae60-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bae60-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bae60-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bae60-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bae60-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="bae60-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

