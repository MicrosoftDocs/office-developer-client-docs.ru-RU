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
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425598"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="cb7f2-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="cb7f2-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="cb7f2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb7f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb7f2-105">Удаляет одну или несколько записей, как правило, пользователей сообщений, списки рассылки или другие контейнеры.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cb7f2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cb7f2-106">Parameters</span></span>

 <span data-ttu-id="cb7f2-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="cb7f2-107">_lpEntries_</span></span>
  
> <span data-ttu-id="cb7f2-108">[in] Указатель на массив структур [ENTRYLIST,](entrylist.md) содержащих идентификаторы записей, которые представляют удаленные записи.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="cb7f2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cb7f2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="cb7f2-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cb7f2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb7f2-111">Return value</span></span>

<span data-ttu-id="cb7f2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb7f2-112">S_OK</span></span> 
  
> <span data-ttu-id="cb7f2-113">Указанные записи успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="cb7f2-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="cb7f2-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="cb7f2-115">Вызов удался, но одну или несколько записей не удалось удалить.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="cb7f2-116">Когда это значение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="cb7f2-117">Чтобы проверить это значение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="cb7f2-118">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="cb7f2-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb7f2-119">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cb7f2-119">MFCMAPI reference</span></span>

<span data-ttu-id="cb7f2-120">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb7f2-121">**Файл**</span><span class="sxs-lookup"><span data-stu-id="cb7f2-121">**File**</span></span>|<span data-ttu-id="cb7f2-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="cb7f2-122">**Function**</span></span>|<span data-ttu-id="cb7f2-123">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="cb7f2-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb7f2-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cb7f2-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="cb7f2-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="cb7f2-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="cb7f2-126">MFCMAPI использует метод **DeleteEntries** для удаления определенной записи из контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cb7f2-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb7f2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cb7f2-127">See also</span></span>



[<span data-ttu-id="cb7f2-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="cb7f2-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="cb7f2-129">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cb7f2-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

