---
title: Имапиформмгрресолвемессажекласс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321611"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="fa558-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="fa558-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="fa558-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa558-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa558-105">Разрешает класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.</span><span class="sxs-lookup"><span data-stu-id="fa558-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="fa558-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa558-106">Parameters</span></span>

 <span data-ttu-id="fa558-107">_Сзмсгкласс_</span><span class="sxs-lookup"><span data-stu-id="fa558-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="fa558-108">возврата Строка, которая указывает имя разрешаемого класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="fa558-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="fa558-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa558-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fa558-110">возврата Битовая маска флагов, определяющих способ разрешения класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa558-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="fa558-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fa558-111">The following flag can be set:</span></span>
    
<span data-ttu-id="fa558-112">МАПИФОРМ_ЕКСАКТМАТЧ</span><span class="sxs-lookup"><span data-stu-id="fa558-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="fa558-113">Необходимо разрешить только строки класса сообщений с точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="fa558-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="fa558-114">_Пфолдерфокус_</span><span class="sxs-lookup"><span data-stu-id="fa558-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="fa558-115">возврата Указатель на папку, в которой находится разрешенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="fa558-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="fa558-116">Параметр _пфолдерфокус_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="fa558-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="fa558-117">_Ппресулт_</span><span class="sxs-lookup"><span data-stu-id="fa558-117">_ppResult_</span></span>
  
> <span data-ttu-id="fa558-118">вышли Указатель на указатель на возвращенный объект сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="fa558-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa558-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa558-119">Return value</span></span>

<span data-ttu-id="fa558-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa558-120">S_OK</span></span> 
  
> <span data-ttu-id="fa558-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="fa558-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fa558-122">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="fa558-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fa558-123">Класс сообщения, переданный в параметре _сзмсгкласс_ , не соответствует классу сообщения для любой формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="fa558-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa558-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="fa558-124">Remarks</span></span>

<span data-ttu-id="fa558-125">Средства просмотра форм вызывают метод **имапиформмгр:: ресолвемессажекласс** , чтобы разрешить класс сообщения в форму в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="fa558-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="fa558-126">Объект сведений о форме, возвращенный в параметре _ппресулт_ , обеспечивает дополнительный доступ к свойствам формы, имеющей заданный класс сообщений.</span><span class="sxs-lookup"><span data-stu-id="fa558-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fa558-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="fa558-127">Notes to callers</span></span>

<span data-ttu-id="fa558-128">Чтобы разрешить класс сообщения в форму, средство просмотра формы передает имя разрешенного класса сообщения, например " `IPM.HelpDesk.Software`".</span><span class="sxs-lookup"><span data-stu-id="fa558-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="fa558-129">Чтобы принудительно разрешить точное решение (то есть, чтобы запретить разрешение для базового класса класса Message при недоступности точного соответствия сервера форм), можно передать флаг МАПИФОРМ_ЕКСАКТМАТЧ в параметр _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="fa558-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="fa558-130">Если параметр _пфолдерфокус_ имеет значение null, процесс разрешения класса Message не выполняет поиск контейнера папок.</span><span class="sxs-lookup"><span data-stu-id="fa558-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="fa558-131">Порядок поиска контейнеров зависит от реализации поставщика библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="fa558-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="fa558-132">Поставщик библиотеки форм по умолчанию выполняет поиск сначала в локальном контейнере, а затем в контейнере папки, в которой находится переданная папка, в контейнере личных форм и в контейнере организации.</span><span class="sxs-lookup"><span data-stu-id="fa558-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="fa558-133">Имена классов сообщений всегда являются строками ANSI, а не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="fa558-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="fa558-134">Идентификатор класса для разрешенного класса сообщения возвращается в составе объекта сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="fa558-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="fa558-135">Средство просмотра форм не должно работать в предположении, что идентификатор класса существует в библиотеке OLE до тех пор, пока средство просмотра форм не вызовет метод [имапиформмгр::P репареформ](imapiformmgr-prepareform.md) или [Имапиформмгр:: креатеформ](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="fa558-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa558-136">См. также</span><span class="sxs-lookup"><span data-stu-id="fa558-136">See also</span></span>



[<span data-ttu-id="fa558-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fa558-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="fa558-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="fa558-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="fa558-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="fa558-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="fa558-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa558-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

