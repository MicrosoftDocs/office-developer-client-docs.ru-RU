---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7fec6b6236d26789a3ec9abee7d2ae1c620f89b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593475"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="4d692-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="4d692-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="4d692-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d692-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d692-105">Сохраняет описание определенной формы в файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4d692-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="4d692-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d692-106">Parameters</span></span>

 <span data-ttu-id="4d692-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="4d692-107">_szFileName_</span></span>
  
> <span data-ttu-id="4d692-108">[in] Строка, имя файла сообщения описание формы, сохранения ее описание.</span><span class="sxs-lookup"><span data-stu-id="4d692-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="4d692-109">Это имя файла должен иметь расширение .fdm.</span><span class="sxs-lookup"><span data-stu-id="4d692-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d692-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4d692-110">Return value</span></span>

<span data-ttu-id="4d692-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4d692-111">S_OK</span></span> 
  
> <span data-ttu-id="4d692-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4d692-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4d692-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="4d692-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="4d692-114">Не удалось записать файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4d692-114">The configuration file could not be written.</span></span> <span data-ttu-id="4d692-115">Чтобы получить структура [MAPIERROR](mapierror.md) , связанный с ошибкой, вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4d692-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="4d692-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4d692-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4d692-117">Возможно, **SaveForm** вызван для сохранения формы в контейнере локального формы.</span><span class="sxs-lookup"><span data-stu-id="4d692-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="4d692-118">**SaveForm** не поддерживается для контейнера локального формы.</span><span class="sxs-lookup"><span data-stu-id="4d692-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4d692-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d692-119">Remarks</span></span>

<span data-ttu-id="4d692-120">Клиентские приложения вызовите метод **IMAPIFormInfo::SaveForm** для сохранения описание текущей формы в файле с заданным именем файла.</span><span class="sxs-lookup"><span data-stu-id="4d692-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="4d692-121">**SaveForm** создает файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4d692-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d692-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4d692-122">Notes to callers</span></span>

<span data-ttu-id="4d692-123">Формы можно установить, выбрав их из списка сообщений дескриптора формы в диалоговом окне, формирующих отображения поставщиков библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4d692-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="4d692-124">Рекомендуемые расширения для сообщений дескриптора формы — .fdm.</span><span class="sxs-lookup"><span data-stu-id="4d692-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="4d692-125">Вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , если **SaveForm** возвращает MAPI_E_EXTENDED_ERROR и проверьте, возвращенные структура **MAPIERROR** для определения условий, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="4d692-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d692-126">См. также</span><span class="sxs-lookup"><span data-stu-id="4d692-126">See also</span></span>



[<span data-ttu-id="4d692-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4d692-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="4d692-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="4d692-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="4d692-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4d692-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

