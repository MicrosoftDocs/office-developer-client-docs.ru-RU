---
title: имсгсторесетрецеивефолдер
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
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434090"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="5c864-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="5c864-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="5c864-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c864-105">Устанавливает папку в качестве назначения для входящих сообщений определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c864-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="5c864-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c864-106">Parameters</span></span>

 <span data-ttu-id="5c864-107">_лпсзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="5c864-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="5c864-108">возврата Указатель на класс сообщений, который необходимо связать с новой папкой получения.</span><span class="sxs-lookup"><span data-stu-id="5c864-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="5c864-109">Если для параметра _лпсзмессажекласс_ ЗАДАНО значение null или пустая строка, **сетрецеивефолдер** устанавливает папку получения по умолчанию для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c864-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="5c864-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c864-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5c864-111">возврата Битовая маска флагов, определяющая тип текста в передаваемых строках.</span><span class="sxs-lookup"><span data-stu-id="5c864-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="5c864-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5c864-112">The following flag can be set:</span></span>
    
<span data-ttu-id="5c864-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c864-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5c864-114">Строка класса сообщения в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="5c864-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="5c864-115">Если флаг MAPI_UNICODE не установлен, строка класса сообщения отображается в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5c864-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="5c864-116">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="5c864-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="5c864-117">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="5c864-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5c864-118">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="5c864-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="5c864-119">возврата Указатель на идентификатор записи папки, которую необходимо установить в качестве папки получения.</span><span class="sxs-lookup"><span data-stu-id="5c864-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="5c864-120">Если для параметра _лпентрид_ ЗАДАНО значение null, **сетрецеивефолдер** заменяет текущую папку получения по умолчанию для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c864-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5c864-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c864-121">Return value</span></span>

<span data-ttu-id="5c864-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c864-122">S_OK</span></span> 
  
> <span data-ttu-id="5c864-123">Папка получения успешно установлена.</span><span class="sxs-lookup"><span data-stu-id="5c864-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c864-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c864-124">Remarks</span></span>

<span data-ttu-id="5c864-125">Метод **IMsgStore:: сетрецеивефолдер** задает или изменяет папку получения для определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c864-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="5c864-126">С помощью **сетрецеивефолдер**клиент может с помощью последовательных вызовов указать другую папку получения для каждого определенного класса сообщений или указать, что входящие сообщения для нескольких классов сообщений отправляются в одну и ту же папку.</span><span class="sxs-lookup"><span data-stu-id="5c864-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="5c864-127">Например, клиент может получить свой собственный класс сообщений в собственной папке.</span><span class="sxs-lookup"><span data-stu-id="5c864-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="5c864-128">Приложение для работы с факсами может обозначать одну папку, в которой поставщик услуг хранения помещает входящие факсы и другую папку, в которой поставщик помещает исходящие факсы.</span><span class="sxs-lookup"><span data-stu-id="5c864-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="5c864-129">Если во время вызова **сетрецеивефолдер**возникает ошибка, параметр папки получения остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="5c864-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="5c864-130">Если **сетрецеивефолдер** изменяет параметр папки получения с _лпентрид_ , для которого задано значение null, указывая, что должна быть задана папка получения по умолчанию, **сетрецеивефолдер** возвращает S_OK, даже если для указанного класса сообщений нет существующего параметра.</span><span class="sxs-lookup"><span data-stu-id="5c864-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5c864-131">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5c864-131">MFCMAPI reference</span></span>

<span data-ttu-id="5c864-132">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5c864-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5c864-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5c864-133">**File**</span></span>|<span data-ttu-id="5c864-134">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5c864-134">**Function**</span></span>|<span data-ttu-id="5c864-135">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5c864-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c864-136">Мсгсторедлг. cpp</span><span class="sxs-lookup"><span data-stu-id="5c864-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="5c864-137">Кмсгсторедлг:: Онсетрецеивефолдер</span><span class="sxs-lookup"><span data-stu-id="5c864-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="5c864-138">MFCMAPI использует метод **IMsgStore:: сетрецеивефолдер** для задания папки в качестве папки получения для определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c864-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c864-139">См. также</span><span class="sxs-lookup"><span data-stu-id="5c864-139">See also</span></span>



[<span data-ttu-id="5c864-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5c864-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="5c864-141">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5c864-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

