---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315500"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="8a564-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a564-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="8a564-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a564-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a564-105">Позволяет поставщику хранилища файлов личных папок (PST) переопределять политику Пстдисаблегров.</span><span class="sxs-lookup"><span data-stu-id="8a564-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a564-106">Наследование от:</span><span class="sxs-lookup"><span data-stu-id="8a564-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="8a564-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="8a564-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="8a564-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8a564-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8a564-109">Поставщик хранилища PST</span><span class="sxs-lookup"><span data-stu-id="8a564-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="8a564-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8a564-110">Called by:</span></span>  <br/> |<span data-ttu-id="8a564-111">Client</span><span class="sxs-lookup"><span data-stu-id="8a564-111">Client</span></span>  <br/> |
|<span data-ttu-id="8a564-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8a564-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8a564-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="8a564-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8a564-114">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="8a564-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8a564-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="8a564-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="8a564-116">Получает список регистраций для файла личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="8a564-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="8a564-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="8a564-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="8a564-118">Регистрирует файлы личных папок для автоматической разблокировки, избегая дальнейших вызовов к Хртрустедпстоверридехандлеркаллбакк.</span><span class="sxs-lookup"><span data-stu-id="8a564-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="8a564-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="8a564-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="8a564-120">Разблокирует файл личных папок для расширения.</span><span class="sxs-lookup"><span data-stu-id="8a564-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a564-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a564-121">Remarks</span></span>

<span data-ttu-id="8a564-122">Идентификаторы интерфейса обработчика переопределения PST-файлов могут быть не определены в текущем загружаемом файле заголовков, в этом случае вы найдете их в разделе [константы MAPI](mapi-constants.md) и можете скопировать их в свой код.</span><span class="sxs-lookup"><span data-stu-id="8a564-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="8a564-123">Используйте макрос DEFINE_GUID, определенный в файле заголовка пакета средств разработки программного обеспечения (SDK) для Microsoft Windows (SDK) guiddef. h, для сопоставления псевдонимов глобального уникального идентификатора (GUID) с их значениями.</span><span class="sxs-lookup"><span data-stu-id="8a564-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="8a564-124">Для получения дополнительных сведений Узнайте, [как реализовать обработчик переопределения PST-файлов, чтобы обойти политику пстдисаблегров в Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="8a564-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a564-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8a564-125">See also</span></span>



[<span data-ttu-id="8a564-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a564-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

