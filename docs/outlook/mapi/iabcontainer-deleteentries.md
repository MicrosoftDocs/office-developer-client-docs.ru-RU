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
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="63835-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="63835-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="63835-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63835-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63835-105">Удаляет одну или несколько записей, обычно для обмена сообщениями пользователей, списков рассылки или других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="63835-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="63835-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63835-106">Parameters</span></span>

 <span data-ttu-id="63835-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="63835-107">_lpEntries_</span></span>
  
> <span data-ttu-id="63835-108">[in] Указатель на массив структур [ENTRYLIST,](entrylist.md) содержащих идентификаторы записей, которые представляют удаляемую запись.</span><span class="sxs-lookup"><span data-stu-id="63835-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="63835-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63835-109">_ulFlags_</span></span>
  
> <span data-ttu-id="63835-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="63835-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63835-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63835-111">Return value</span></span>

<span data-ttu-id="63835-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="63835-112">S_OK</span></span> 
  
> <span data-ttu-id="63835-113">Указанные записи успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="63835-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="63835-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="63835-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="63835-115">Вызов был успешным, но не удалось удалить одну или несколько записей.</span><span class="sxs-lookup"><span data-stu-id="63835-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="63835-116">При возвращении этого значения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="63835-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="63835-117">Чтобы проверить это значение,  используйте HR_FAILED макрос.</span><span class="sxs-lookup"><span data-stu-id="63835-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="63835-118">Дополнительные сведения см. в теме ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="63835-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="63835-119">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="63835-119">MFCMAPI reference</span></span>

<span data-ttu-id="63835-120">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="63835-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="63835-121">**Файл**</span><span class="sxs-lookup"><span data-stu-id="63835-121">**File**</span></span>|<span data-ttu-id="63835-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="63835-122">**Function**</span></span>|<span data-ttu-id="63835-123">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="63835-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63835-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="63835-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="63835-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="63835-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="63835-126">MFCMAPI использует метод **DeleteEntries** для удаления определенной записи из контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="63835-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63835-127">См. также</span><span class="sxs-lookup"><span data-stu-id="63835-127">See also</span></span>



[<span data-ttu-id="63835-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="63835-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="63835-129">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="63835-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

