---
title: Имапиформконтаинерресолвемултиплемессажеклассес
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342184"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="95995-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="95995-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="95995-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95995-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95995-105">Разрешает группу классов сообщений в свои формы в контейнере формы и возвращает массив объектов данных формы для этих форм.</span><span class="sxs-lookup"><span data-stu-id="95995-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="95995-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95995-106">Parameters</span></span>

 <span data-ttu-id="95995-107">_Пмсгклассаррай_</span><span class="sxs-lookup"><span data-stu-id="95995-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="95995-108">возврата Указатель на массив, содержащий имена классов сообщений, которые требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="95995-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="95995-109">Имена классов сообщений всегда являются строками ANSI, а не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="95995-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="95995-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95995-110">_ulFlags_</span></span>
  
> <span data-ttu-id="95995-111">возврата Битовая маска флагов, определяющих способ разрешения классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="95995-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="95995-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="95995-112">The following flag can be set:</span></span>
    
<span data-ttu-id="95995-113">МАПИФОРМ_ЕКСАКТМАТЧ</span><span class="sxs-lookup"><span data-stu-id="95995-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="95995-114">Необходимо разрешить только строки класса сообщений с точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="95995-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="95995-115">_ппфрминфоаррай_</span><span class="sxs-lookup"><span data-stu-id="95995-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="95995-116">вышли Указатель на указатель на массив объектов сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="95995-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="95995-117">Если клиентское приложение передает значение NULL в параметр _пмсгклассаррай_ , параметр _ппфрминфоаррай_ содержит объекты информации формы для всех форм в контейнере.</span><span class="sxs-lookup"><span data-stu-id="95995-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="95995-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95995-118">Return value</span></span>

<span data-ttu-id="95995-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="95995-119">S_OK</span></span> 
  
> <span data-ttu-id="95995-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="95995-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95995-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95995-121">Remarks</span></span>

<span data-ttu-id="95995-122">Клиентские приложения вызывают метод **имапиформконтаинер:: ресолвемултиплемессажеклассес** для разрешения группы классов сообщений в формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="95995-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="95995-123">Массив объектов данных формы, возвращаемых в параметре _ппфрминфоаррай_ , обеспечивает дополнительный доступ к каждому из свойств формы.</span><span class="sxs-lookup"><span data-stu-id="95995-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="95995-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="95995-124">Notes to callers</span></span>

<span data-ttu-id="95995-125">Чтобы разрешить группу классов сообщений формам, передайте массив имен классов сообщений, которые требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="95995-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="95995-126">Чтобы принудительно разрешить точное решение (то есть, чтобы предотвратить разрешение для базового класса класса Message), можно передать флаг МАПИФОРМ_ЕКСАКТМАТЧ в параметр _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="95995-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="95995-127">Если класс сообщения невозможно разрешить в форму, возвращается значение NULL для этого класса сообщения в массиве данных формы.</span><span class="sxs-lookup"><span data-stu-id="95995-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="95995-128">Таким образом, даже если метод возвращает значение S_OK, не следует предполагать, что все классы сообщений успешно разрешены.</span><span class="sxs-lookup"><span data-stu-id="95995-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="95995-129">Вместо этого проверьте значения в возвращенном массиве.</span><span class="sxs-lookup"><span data-stu-id="95995-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="95995-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="95995-130">MFCMAPI reference</span></span>

<span data-ttu-id="95995-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="95995-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="95995-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="95995-132">**File**</span></span>|<span data-ttu-id="95995-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="95995-133">**Function**</span></span>|<span data-ttu-id="95995-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="95995-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="95995-135">Формконтаинердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="95995-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="95995-136">Кформконтаинердлг:: Онресолвемултиплемессажеклассес</span><span class="sxs-lookup"><span data-stu-id="95995-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="95995-137">MFCMAPI использует метод **имапиформконтаинер:: ресолвемултиплемессажеклассес** для обнаружения формы, связанной с набором классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="95995-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95995-138">См. также</span><span class="sxs-lookup"><span data-stu-id="95995-138">See also</span></span>



[<span data-ttu-id="95995-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="95995-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="95995-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95995-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="95995-141">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="95995-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

