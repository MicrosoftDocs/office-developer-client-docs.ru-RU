---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c744407790fecde6b6d89dff669ea4db07ce7701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808707"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="aceac-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="aceac-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="aceac-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aceac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aceac-105">Удаляет один или несколько операций, обычно системы обмена сообщениями пользователи, списков рассылки или других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="aceac-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="aceac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aceac-106">Parameters</span></span>

 <span data-ttu-id="aceac-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="aceac-107">_lpEntries_</span></span>
  
> <span data-ttu-id="aceac-108">[in] Указатель на массив структур [ENTRYLIST](entrylist.md) , которые содержат идентификаторы записей, которые представляют операции удаления.</span><span class="sxs-lookup"><span data-stu-id="aceac-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="aceac-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aceac-109">_ulFlags_</span></span>
  
> <span data-ttu-id="aceac-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="aceac-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aceac-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="aceac-111">Return value</span></span>

<span data-ttu-id="aceac-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="aceac-112">S_OK</span></span> 
  
> <span data-ttu-id="aceac-113">Указанные записи успешно удален.</span><span class="sxs-lookup"><span data-stu-id="aceac-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="aceac-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="aceac-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="aceac-115">Вызов завершился успешно, но не удалось удалить один или несколько записей.</span><span class="sxs-lookup"><span data-stu-id="aceac-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="aceac-116">При возвращении это значение вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="aceac-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="aceac-117">Чтобы проверить это значение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="aceac-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="aceac-118">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="aceac-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="aceac-119">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="aceac-119">MFCMAPI reference</span></span>

<span data-ttu-id="aceac-120">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="aceac-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aceac-121">**����**</span><span class="sxs-lookup"><span data-stu-id="aceac-121">**File**</span></span>|<span data-ttu-id="aceac-122">**�������**</span><span class="sxs-lookup"><span data-stu-id="aceac-122">**Function**</span></span>|<span data-ttu-id="aceac-123">**�����������**</span><span class="sxs-lookup"><span data-stu-id="aceac-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aceac-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="aceac-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="aceac-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="aceac-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="aceac-126">Mfcmapi (en) метод **внешнее** используется для удаления конкретную запись из контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="aceac-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aceac-127">См. также</span><span class="sxs-lookup"><span data-stu-id="aceac-127">See also</span></span>



[<span data-ttu-id="aceac-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="aceac-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="aceac-129">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="aceac-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

