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
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="2f907-103">Каноническое свойство PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="2f907-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="2f907-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f907-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f907-105">Указывает имя видимой пользователем учетной записи электронной почты, через которую отправляется сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2f907-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f907-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2f907-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f907-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="2f907-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="2f907-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2f907-108">Property set:</span></span>  <br/> |<span data-ttu-id="2f907-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2f907-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2f907-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="2f907-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2f907-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="2f907-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="2f907-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2f907-112">Data type:</span></span>  <br/> |<span data-ttu-id="2f907-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2f907-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2f907-114">Область:</span><span class="sxs-lookup"><span data-stu-id="2f907-114">Area:</span></span>  <br/> |<span data-ttu-id="2f907-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="2f907-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f907-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f907-116">Remarks</span></span>

<span data-ttu-id="2f907-117">Формат этой строки зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="2f907-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="2f907-118">Это свойство может использоваться клиентом для определения сервера, на который направляется почта, но является необязательным, а значение не имеет значения для сервера.</span><span class="sxs-lookup"><span data-stu-id="2f907-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2f907-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2f907-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f907-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2f907-120">Protocol specifications</span></span>

<span data-ttu-id="2f907-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f907-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f907-122">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="2f907-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f907-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f907-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f907-124">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2f907-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f907-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="2f907-125">Header files</span></span>

<span data-ttu-id="2f907-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f907-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f907-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2f907-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f907-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2f907-128">See also</span></span>



[<span data-ttu-id="2f907-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2f907-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f907-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2f907-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f907-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2f907-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f907-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2f907-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

