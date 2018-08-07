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
ms.openlocfilehash: f58bd8499b63bcd526906f78143b76092f194cb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809373"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="e3e6d-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="e3e6d-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="e3e6d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3e6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3e6d-105">Получает к папке, где были установлены как место назначения для входящих сообщений из указанного класса сообщений или по умолчанию получают папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="e3e6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3e6d-106">Parameters</span></span>

 <span data-ttu-id="e3e6d-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="e3e6d-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="e3e6d-108">[in] Указатель на класс сообщений, который связан с папкой получения.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="e3e6d-109">Если параметр _lpszMessageClass_ имеет значение NULL или пустая строка, **GetReceiveFolder** возвращает значение по умолчанию получают папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="e3e6d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3e6d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e3e6d-111">[in] Битовая маска флаги, определяющее тип переданное и возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="e3e6d-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e3e6d-112">The following flag can be set:</span></span>
    
<span data-ttu-id="e3e6d-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e3e6d-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e3e6d-114">— Это строка класс сообщения в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="e3e6d-115">Если флаг MAPI_UNICODE не установлен, — это строка класс сообщения в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="e3e6d-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e3e6d-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="e3e6d-117">[out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e3e6d-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e3e6d-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="e3e6d-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="e3e6d-119">[out] Указатель на указатель на идентификатор записи для запрошенного получать папку.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="e3e6d-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="e3e6d-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="e3e6d-121">[out] Указатель на указатель на класс сообщения, явно задает в качестве его получать папку папке указывает _lppEntryID_.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="e3e6d-122">Этот класс сообщения должны быть то же, что класс с помощью параметра _lpszMessageClass_ или базового класса этого класса.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="e3e6d-123">Значение NULL указывает, что папка, на который указывает _lppEntryID_ по умолчанию получают папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e3e6d-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="e3e6d-124">Return value</span></span>

<span data-ttu-id="e3e6d-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e3e6d-125">S_OK</span></span> 
  
> <span data-ttu-id="e3e6d-126">Папку получения успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3e6d-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="e3e6d-127">Remarks</span></span>

<span data-ttu-id="e3e6d-128">Метод **IMsgStore::GetReceiveFolder** Получает идентификатор записи папки получения, папки, предназначенный для получения входящих сообщений класса определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="e3e6d-129">С помощью параметра _lpszMessageClass_ абонентов можно указать класс сообщения или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="e3e6d-130">Если _lpszMessageClass_ имеет значение NULL, **GetReceiveFolder** возвращает следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e3e6d-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="e3e6d-131">В _lppszExplicitClass_имя класса первоначального базового класса сообщений указывает явно задать папку получения _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="e3e6d-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="e3e6d-132">В _lppEntryID_идентификатор записи папки получения для базового класса, на который указывает с помощью параметра _lppszExplicitClass_ .</span><span class="sxs-lookup"><span data-stu-id="e3e6d-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="e3e6d-133">Предположим, например, папку получения класс сообщения **IPM. Примечание** имеет значение записи идентификатор папки "Входящие" и **GetReceiveFolder** вызывается с содержимым _lpszMessageClass_ значение **IPM. Note.Phone**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="e3e6d-134">Если **IPM. Note.Phone** не имеют явно получает набор папок, **GetReceiveFolder** возвращает идентификатор записи из папки «Входящие» в _lppEntryID_ и **IPM. Примечание** в _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="e3e6d-135">Если клиент вызывает **GetReceiveFolder** для класса сообщений и не установлен в папку получения для этого класса сообщений, _lppszExplicitClass_ — это строка нулевой длины, string в формате Юникод или строку в формате ANSI в зависимости от того, требуется ли клиент задан флаг MAPI_UNICODE в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="e3e6d-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="e3e6d-136">По умолчанию получение папки, полученного с передачей NULL в параметре _lpszMessageClass_ , всегда существует для каждого хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="e3e6d-137">Клиента необходимо вызвать функцию [MAPIFreeBuffer](mapifreebuffer.md) , когда это делается с идентификатором записи, возвращаемых в _lppEntryID_ , чтобы освободить память, в котором размещается этот идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="e3e6d-138">Он также вызвать **MAPIFreeBuffer** при завершении со строки класс сообщения, возвращаемые в _lppszExplicitClass_ , чтобы освободить память, в котором размещается этой строки.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e3e6d-139">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="e3e6d-139">MFCMAPI reference</span></span>

<span data-ttu-id="e3e6d-140">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e3e6d-141">**����**</span><span class="sxs-lookup"><span data-stu-id="e3e6d-141">**File**</span></span>|<span data-ttu-id="e3e6d-142">**�������**</span><span class="sxs-lookup"><span data-stu-id="e3e6d-142">**Function**</span></span>|<span data-ttu-id="e3e6d-143">**�����������**</span><span class="sxs-lookup"><span data-stu-id="e3e6d-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3e6d-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e3e6d-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e3e6d-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="e3e6d-145">GetInbox</span></span>  <br/> |<span data-ttu-id="e3e6d-146">Mfcmapi (en) использует метод **IMsgStore::GetReceiveFolder** найти папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="e3e6d-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3e6d-147">См. также</span><span class="sxs-lookup"><span data-stu-id="e3e6d-147">See also</span></span>



[<span data-ttu-id="e3e6d-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e3e6d-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e3e6d-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e3e6d-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="e3e6d-150">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e3e6d-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

