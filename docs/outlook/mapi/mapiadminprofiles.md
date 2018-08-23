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
# <a name="mapiadminprofiles"></a><span data-ttu-id="c8795-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="c8795-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="c8795-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8795-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8795-105">Создает объект администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="c8795-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8795-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c8795-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8795-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="c8795-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c8795-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="c8795-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c8795-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c8795-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c8795-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="c8795-110">Called by:</span></span>  <br/> |<span data-ttu-id="c8795-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="c8795-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="c8795-112">���������</span><span class="sxs-lookup"><span data-stu-id="c8795-112">Parameters</span></span>

 <span data-ttu-id="c8795-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8795-113">_ulFlags_</span></span>
  
> <span data-ttu-id="c8795-114">[in] Битовая маска, указывающее параметры для функции входа службы флагов.</span><span class="sxs-lookup"><span data-stu-id="c8795-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="c8795-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="c8795-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="c8795-116">[out] Указатель на указатель на новый объект администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="c8795-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8795-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c8795-117">Return value</span></span>

<span data-ttu-id="c8795-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c8795-118">S_OK</span></span> 
  
> <span data-ttu-id="c8795-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c8795-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c8795-120">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="c8795-120">MFCMAPI reference</span></span>

<span data-ttu-id="c8795-121">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="c8795-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c8795-122">**����**</span><span class="sxs-lookup"><span data-stu-id="c8795-122">**File**</span></span>|<span data-ttu-id="c8795-123">**�������**</span><span class="sxs-lookup"><span data-stu-id="c8795-123">**Function**</span></span>|<span data-ttu-id="c8795-124">**�����������**</span><span class="sxs-lookup"><span data-stu-id="c8795-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8795-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="c8795-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="c8795-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="c8795-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="c8795-127">Mfcmapi (en) использует метод **MAPIAdminProfiles** для получения объекта администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="c8795-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8795-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c8795-128">See also</span></span>



[<span data-ttu-id="c8795-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="c8795-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="c8795-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c8795-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

