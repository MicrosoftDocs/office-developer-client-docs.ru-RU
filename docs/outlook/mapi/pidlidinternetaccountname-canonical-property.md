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
ms.openlocfilehash: ac47f150ebdd39ed5f2abe4b30a2cac5768fd229
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565132"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="edbd1-103">Каноническое свойство PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="edbd1-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="edbd1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edbd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edbd1-105">Указывает имя учетной записи электронной почты видимыми, через который отправляется сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="edbd1-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edbd1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="edbd1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edbd1-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="edbd1-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="edbd1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="edbd1-108">Property set:</span></span>  <br/> |<span data-ttu-id="edbd1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="edbd1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="edbd1-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="edbd1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="edbd1-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="edbd1-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="edbd1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="edbd1-112">Data type:</span></span>  <br/> |<span data-ttu-id="edbd1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="edbd1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="edbd1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="edbd1-114">Area:</span></span>  <br/> |<span data-ttu-id="edbd1-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="edbd1-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edbd1-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="edbd1-116">Remarks</span></span>

<span data-ttu-id="edbd1-117">Формат этой строки — зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="edbd1-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="edbd1-118">Это свойство можно использовать клиента, чтобы определить, какой сервер для направления почтовое приложение должно, но является необязательным, и значение не имеет значения для сервера.</span><span class="sxs-lookup"><span data-stu-id="edbd1-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edbd1-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="edbd1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edbd1-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="edbd1-120">Protocol specifications</span></span>

<span data-ttu-id="edbd1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edbd1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edbd1-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="edbd1-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edbd1-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edbd1-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edbd1-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="edbd1-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edbd1-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="edbd1-125">Header files</span></span>

<span data-ttu-id="edbd1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edbd1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="edbd1-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="edbd1-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edbd1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="edbd1-128">See also</span></span>



[<span data-ttu-id="edbd1-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="edbd1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edbd1-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="edbd1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edbd1-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="edbd1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edbd1-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="edbd1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

