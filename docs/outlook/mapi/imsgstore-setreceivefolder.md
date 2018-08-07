---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c30c38e1dbc944fd3016badf2621aef5de1e08f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809404"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="b5621-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="b5621-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="b5621-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5621-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5621-105">Устанавливает папки в качестве назначения для входящих сообщений класса определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5621-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="b5621-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5621-106">Parameters</span></span>

 <span data-ttu-id="b5621-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="b5621-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="b5621-108">[in] Указатель на класс сообщений, который необходимо связать с новым получать папку.</span><span class="sxs-lookup"><span data-stu-id="b5621-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="b5621-109">Если параметр _lpszMessageClass_ имеет значение NULL или пустая строка, **SetReceiveFolder** наборов по умолчанию получают папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="b5621-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="b5621-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b5621-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b5621-111">[in] Битовая маска флаги, определяющее тип текста в строках переданное.</span><span class="sxs-lookup"><span data-stu-id="b5621-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="b5621-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b5621-112">The following flag can be set:</span></span>
    
<span data-ttu-id="b5621-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b5621-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b5621-114">— Это строка класс сообщения в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b5621-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="b5621-115">Если флаг MAPI_UNICODE не установлен, — это строка класс сообщения в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b5621-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="b5621-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b5621-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="b5621-117">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b5621-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b5621-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b5621-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="b5621-119">[in] Указатель на идентификатор записи папки, чтобы определить, папку получения.</span><span class="sxs-lookup"><span data-stu-id="b5621-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="b5621-120">Если параметр _lpEntryID_ имеет значение NULL, **SetReceiveFolder** заменяет текущий получать папку с хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5621-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b5621-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="b5621-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b5621-122">S_OK</span></span> 
  
> <span data-ttu-id="b5621-123">Получение папки успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="b5621-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5621-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="b5621-124">Remarks</span></span>

<span data-ttu-id="b5621-125">Метод **IMsgStore::SetReceiveFolder** задает или изменяет папку получения для класса определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5621-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="b5621-126">С помощью **SetReceiveFolder**клиента можно с помощью последовательных вызовов указать другой получать папки для каждого сообщения определенного класса или указать, что входящие сообщения для всех несколько классов сообщений перейдите к папке.</span><span class="sxs-lookup"><span data-stu-id="b5621-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="b5621-127">Например клиент может иметь собственный класс сообщения поступают в отдельную папку.</span><span class="sxs-lookup"><span data-stu-id="b5621-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="b5621-128">Приложение факсов можно назначить одну папку Входящие факсы помещает его поставщика хранилища и другую папку, в которой поставщик помещает исходящих факсов.</span><span class="sxs-lookup"><span data-stu-id="b5621-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="b5621-129">При возникновении ошибки во время вызова **SetReceiveFolder**, Настройка папки получения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b5621-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="b5621-130">При изменении **SetReceiveFolder** параметр папку получения с _lpEntryID_ имеет значение NULL, указывающего на то, что необходимо задать папку получения по умолчанию, **SetReceiveFolder** возвращает значение S_OK даже в том случае, если не было отсутствуют существующие параметры для указанного Класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5621-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b5621-131">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="b5621-131">MFCMAPI reference</span></span>

<span data-ttu-id="b5621-132">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="b5621-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b5621-133">**����**</span><span class="sxs-lookup"><span data-stu-id="b5621-133">**File**</span></span>|<span data-ttu-id="b5621-134">**�������**</span><span class="sxs-lookup"><span data-stu-id="b5621-134">**Function**</span></span>|<span data-ttu-id="b5621-135">**�����������**</span><span class="sxs-lookup"><span data-stu-id="b5621-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b5621-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b5621-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="b5621-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="b5621-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="b5621-138">Mfcmapi (en) использует метод **IMsgStore::SetReceiveFolder** для установки в папку в папку получения для класса определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5621-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5621-139">См. также</span><span class="sxs-lookup"><span data-stu-id="b5621-139">See also</span></span>



[<span data-ttu-id="b5621-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b5621-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="b5621-141">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b5621-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

