---
title: Имапиформконтаинерресолвемессажекласс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408553"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="fbff7-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="fbff7-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="fbff7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbff7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbff7-105">Разрешает класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.</span><span class="sxs-lookup"><span data-stu-id="fbff7-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="fbff7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbff7-106">Parameters</span></span>

 <span data-ttu-id="fbff7-107">_Сзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="fbff7-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="fbff7-108">возврата Строка, которая указывает имя разрешаемого класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="fbff7-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="fbff7-109">Имена классов сообщений всегда являются строками ANSI, а не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="fbff7-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="fbff7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fbff7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="fbff7-111">возврата Битовая маска флагов, определяющих способ разрешения класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="fbff7-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="fbff7-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fbff7-112">The following flag can be set:</span></span>
    
<span data-ttu-id="fbff7-113">МАПИФОРМ_ЕКСАКТМАТЧ</span><span class="sxs-lookup"><span data-stu-id="fbff7-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="fbff7-114">Необходимо разрешить только строки класса сообщений с точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="fbff7-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="fbff7-115">_ппформинфо_</span><span class="sxs-lookup"><span data-stu-id="fbff7-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="fbff7-116">вышли Указатель на указатель на возвращенный объект сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="fbff7-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fbff7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbff7-117">Return value</span></span>

<span data-ttu-id="fbff7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbff7-118">S_OK</span></span> 
  
> <span data-ttu-id="fbff7-119">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="fbff7-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fbff7-120">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="fbff7-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fbff7-121">Класс сообщения, переданный в параметре _сзмессажекласс_ , не соответствует классу сообщения для любой формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="fbff7-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fbff7-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbff7-122">Remarks</span></span>

<span data-ttu-id="fbff7-123">Клиентские приложения вызывают метод **имапиформконтаинер:: ресолвемессажекласс** для разрешения класса сообщений в форму в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="fbff7-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="fbff7-124">Объект сведений о форме, возвращенный в параметре _ппформинфо_ , предоставляет дополнительный доступ к свойствам формы с заданным классом Message.</span><span class="sxs-lookup"><span data-stu-id="fbff7-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fbff7-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="fbff7-125">Notes to callers</span></span>

<span data-ttu-id="fbff7-126">Чтобы разрешить класс сообщения в форму, передайте имя разрешенного класса сообщения (например, `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="fbff7-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="fbff7-127">Чтобы принудительно разрешить точное решение (то есть, чтобы предотвратить разрешение для базового класса класса Message), можно передать флаг МАПИФОРМ_ЕКСАКТМАТЧ в параметр _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="fbff7-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="fbff7-128">Идентификатор класса для разрешенного класса сообщения возвращается в составе объекта сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="fbff7-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="fbff7-129">Не следует предполагать, что идентификатор класса существует в библиотеке OLE до тех пор, пока не будет вызван метод [имапиформмгр::P репареформ](imapiformmgr-prepareform.md) или [Имапиформмгр:: креатеформ](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="fbff7-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fbff7-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fbff7-130">MFCMAPI reference</span></span>

<span data-ttu-id="fbff7-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="fbff7-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fbff7-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="fbff7-132">**File**</span></span>|<span data-ttu-id="fbff7-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="fbff7-133">**Function**</span></span>|<span data-ttu-id="fbff7-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="fbff7-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fbff7-135">Формконтаинердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="fbff7-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="fbff7-136">Кформконтаинердлг:: Онресолвемессажекласс</span><span class="sxs-lookup"><span data-stu-id="fbff7-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="fbff7-137">MFCMAPI использует метод **имапиформконтаинер:: ресолвемессажекласс** для обнаружения формы, связанной с классом сообщений.</span><span class="sxs-lookup"><span data-stu-id="fbff7-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbff7-138">См. также</span><span class="sxs-lookup"><span data-stu-id="fbff7-138">See also</span></span>



[<span data-ttu-id="fbff7-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fbff7-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="fbff7-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="fbff7-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="fbff7-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="fbff7-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="fbff7-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fbff7-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

