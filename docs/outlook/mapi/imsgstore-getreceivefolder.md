---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435350"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="1d88c-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="1d88c-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="1d88c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d88c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d88c-105">Получает папку, которая была установлена в качестве назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1d88c-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="1d88c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1d88c-106">Parameters</span></span>

 <span data-ttu-id="1d88c-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="1d88c-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="1d88c-108">[in] Указатель на класс сообщений, связанный с папкой получения.</span><span class="sxs-lookup"><span data-stu-id="1d88c-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="1d88c-109">Если параметр  _lpszMessageClass_ задан для NULL или пустой строки, **GetReceiveFolder** возвращает папку получения по умолчанию для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1d88c-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="1d88c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d88c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1d88c-111">[in] Битмашка флагов, которые контролируют тип переданных и возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="1d88c-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="1d88c-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="1d88c-112">The following flag can be set:</span></span>
    
<span data-ttu-id="1d88c-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d88c-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1d88c-114">Строка класса сообщения находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="1d88c-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="1d88c-115">Если флаг MAPI_UNICODE не установлен, строка класса сообщения находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1d88c-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="1d88c-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1d88c-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="1d88c-117">[вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="1d88c-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1d88c-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="1d88c-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="1d88c-119">[вышел] Указатель на указатель на идентификатор записи для запрашиваемой папки получения.</span><span class="sxs-lookup"><span data-stu-id="1d88c-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="1d88c-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="1d88c-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="1d88c-121">[вышел] Указатель на указатель класса сообщений, который явно задает в качестве папки получения папку, на которую указывает _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="1d88c-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="1d88c-122">Этот класс сообщений должен быть таким же, как класс в параметре  _lpszMessageClass,_ или базовым классом этого класса.</span><span class="sxs-lookup"><span data-stu-id="1d88c-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="1d88c-123">Передача NULL указывает, что папка, на которую указывает  _lppEntryID,_ является папкой получения по умолчанию для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1d88c-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d88c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d88c-124">Return value</span></span>

<span data-ttu-id="1d88c-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d88c-125">S_OK</span></span> 
  
> <span data-ttu-id="1d88c-126">Папка получения успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="1d88c-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d88c-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d88c-127">Remarks</span></span>

<span data-ttu-id="1d88c-128">Метод **IMsgStore::GetReceiveFolder** получает идентификатор входа папки получения, папки, предназначенной для получения входящих сообщений определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="1d88c-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="1d88c-129">Звонители могут указать класс сообщения или NULL в _параметре lpszMessageClass._</span><span class="sxs-lookup"><span data-stu-id="1d88c-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="1d88c-130">Если  _lpszMessageClass_ является NULL, **GetReceiveFolder** возвращает следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1d88c-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="1d88c-131">В  _lppszExplicitClass_ имя первого базового класса класса сообщений, на которое указывает  _lpszMessageClass,_ явно устанавливая папку получения.</span><span class="sxs-lookup"><span data-stu-id="1d88c-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="1d88c-132">В _lppEntryID_ идентификатор записи папки получения для базового класса указывается _параметром lppszExplicitClass._</span><span class="sxs-lookup"><span data-stu-id="1d88c-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="1d88c-133">Например, предположим, что папка **IPM класса сообщений принимается. Примечание** установлено для идентификатора входа в почтовый ящик, и **GetReceiveFolder** называется с содержимым _lpszMessageClass,_ установленным **для IPM. Примечание. Телефон**.</span><span class="sxs-lookup"><span data-stu-id="1d88c-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="1d88c-134">Если **IPM. Примечание. Телефон** не имеет явного набора папок получения, **GetReceiveFolder** возвращает идентификатор входа в папке "Входящие" в _lppEntryID_ и **IPM. Примечание** в _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="1d88c-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="1d88c-135">Если клиент вызывает **GetReceiveFolder** для класса сообщений и не задает папку получения для этого класса сообщений, _lppszExplicitClass_ — это строка нулевой длины, строка в формате Unicode или строка в формате ANSI в зависимости от того, установил ли клиент флаг MAPI_UNICODE в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="1d88c-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="1d88c-136">Папка получения по умолчанию, полученная путем передачи NULL в  _параметре lpszMessageClass,_ всегда существует для каждого магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1d88c-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="1d88c-137">Клиент должен вызвать функцию [MAPIFreeBuffer,](mapifreebuffer.md) когда она будет сделана с идентификатором записи, возвращенным  _в lppEntryID,_ чтобы освободить память, которая содержит этот идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="1d88c-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="1d88c-138">Следует также вызвать **MAPIFreeBuffer,** когда это будет сделано со строкой класса сообщений, возвращаемой в  _lppszExplicitClass,_ чтобы освободить память, которая содержит эту строку.</span><span class="sxs-lookup"><span data-stu-id="1d88c-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d88c-139">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1d88c-139">MFCMAPI reference</span></span>

<span data-ttu-id="1d88c-140">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1d88c-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d88c-141">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1d88c-141">**File**</span></span>|<span data-ttu-id="1d88c-142">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1d88c-142">**Function**</span></span>|<span data-ttu-id="1d88c-143">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1d88c-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d88c-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1d88c-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1d88c-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="1d88c-145">GetInbox</span></span>  <br/> |<span data-ttu-id="1d88c-146">MFCMAPI использует **метод IMsgStore::GetReceiveFolder** для обнаружения папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="1d88c-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d88c-147">См. также</span><span class="sxs-lookup"><span data-stu-id="1d88c-147">See also</span></span>



[<span data-ttu-id="1d88c-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1d88c-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1d88c-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1d88c-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="1d88c-150">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1d88c-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

