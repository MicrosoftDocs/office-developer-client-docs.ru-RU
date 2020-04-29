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
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412354"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="7cdc2-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="7cdc2-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="7cdc2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cdc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cdc2-105">Создает объект администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="7cdc2-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7cdc2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7cdc2-106">Header file:</span></span>  <br/> |<span data-ttu-id="7cdc2-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="7cdc2-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="7cdc2-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7cdc2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7cdc2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7cdc2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7cdc2-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7cdc2-110">Called by:</span></span>  <br/> |<span data-ttu-id="7cdc2-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="7cdc2-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="7cdc2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cdc2-112">Parameters</span></span>

 <span data-ttu-id="7cdc2-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7cdc2-113">_ulFlags_</span></span>
  
> <span data-ttu-id="7cdc2-114">возврата Битовая маска флагов, указывающих параметры функции записи службы.</span><span class="sxs-lookup"><span data-stu-id="7cdc2-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="7cdc2-115">_лпппрофадмин_</span><span class="sxs-lookup"><span data-stu-id="7cdc2-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="7cdc2-116">вышли Указатель на указатель на новый объект администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="7cdc2-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7cdc2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cdc2-117">Return value</span></span>

<span data-ttu-id="7cdc2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7cdc2-118">S_OK</span></span> 
  
> <span data-ttu-id="7cdc2-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7cdc2-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7cdc2-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7cdc2-120">MFCMAPI reference</span></span>

<span data-ttu-id="7cdc2-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7cdc2-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7cdc2-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7cdc2-122">**File**</span></span>|<span data-ttu-id="7cdc2-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7cdc2-123">**Function**</span></span>|<span data-ttu-id="7cdc2-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7cdc2-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cdc2-125">Мапиобжектс. cpp</span><span class="sxs-lookup"><span data-stu-id="7cdc2-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="7cdc2-126">Кмапиобжектс:: Жетпрофадмин</span><span class="sxs-lookup"><span data-stu-id="7cdc2-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="7cdc2-127">MFCMAPI использует метод **мапиадминпрофилес** , чтобы получить объект администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="7cdc2-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cdc2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7cdc2-128">See also</span></span>



[<span data-ttu-id="7cdc2-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="7cdc2-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="7cdc2-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7cdc2-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

