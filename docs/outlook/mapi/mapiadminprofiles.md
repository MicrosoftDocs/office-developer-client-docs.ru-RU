---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581288"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="0f3b1-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="0f3b1-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="0f3b1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f3b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f3b1-105">Создает объект администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="0f3b1-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f3b1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0f3b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f3b1-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="0f3b1-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="0f3b1-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0f3b1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f3b1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0f3b1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0f3b1-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0f3b1-110">Called by:</span></span>  <br/> |<span data-ttu-id="0f3b1-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="0f3b1-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="0f3b1-112">���������</span><span class="sxs-lookup"><span data-stu-id="0f3b1-112">Parameters</span></span>

 <span data-ttu-id="0f3b1-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f3b1-113">_ulFlags_</span></span>
  
> <span data-ttu-id="0f3b1-114">[in] Битовая маска, указывающее параметры для функции входа службы флагов.</span><span class="sxs-lookup"><span data-stu-id="0f3b1-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="0f3b1-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="0f3b1-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="0f3b1-116">[out] Указатель на указатель на новый объект администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="0f3b1-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f3b1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f3b1-117">Return value</span></span>

<span data-ttu-id="0f3b1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f3b1-118">S_OK</span></span> 
  
> <span data-ttu-id="0f3b1-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0f3b1-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0f3b1-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0f3b1-120">MFCMAPI reference</span></span>

<span data-ttu-id="0f3b1-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0f3b1-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0f3b1-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0f3b1-122">**File**</span></span>|<span data-ttu-id="0f3b1-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0f3b1-123">**Function**</span></span>|<span data-ttu-id="0f3b1-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0f3b1-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f3b1-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="0f3b1-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="0f3b1-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="0f3b1-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="0f3b1-127">Mfcmapi (en) использует метод **MAPIAdminProfiles** для получения объекта администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="0f3b1-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f3b1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0f3b1-128">See also</span></span>



[<span data-ttu-id="0f3b1-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="0f3b1-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="0f3b1-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0f3b1-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

